---
description: 'Дополнительные сведения о: TN068: выполнение транзакций с помощью драйвера ODBC для Microsoft Access 7'
title: TN068. Выполнение транзакций с драйвером Microsoft Access 7 ODBC
ms.date: 06/28/2018
f1_keywords:
- vc.data.odbc
helpviewer_keywords:
- TN068 [MFC]
- transactions [MFC], calling BeginTrans
- transactions [MFC], Microsoft Access
ms.assetid: d3f8f5d9-b118-4194-be36-a1aefb630c45
ms.openlocfilehash: ebc98a0fd2bea78c0159daa9a53a11a292482257
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97214550"
---
# <a name="tn068-performing-transactions-with-the-microsoft-access-7-odbc-driver"></a>TN068. Выполнение транзакций с драйвером Microsoft Access 7 ODBC

> [!NOTE]
> Следующее техническое примечание не было обновлено, поскольку сначала оно было включено в электронную документацию. В результате некоторые процедуры и разделы могут быть устаревшими или неверными. Для получения последних сведений рекомендуется выполнить поиск интересующей темы в алфавитном указателе документации в Интернете.

В этом заметке описывается выполнение транзакций при использовании классов базы данных ODBC MFC и драйвера ODBC для Microsoft Access 7,0, входящего в пакет драйверов Microsoft ODBC для рабочих столов версии 3,0.

## <a name="overview"></a>Общие сведения

Если приложение базы данных выполняет транзакции, необходимо соблюдать осторожность при вызове `CDatabase::BeginTrans` и `CRecordset::Open` в правильной последовательности в приложении. Драйвер Microsoft Access 7,0 использует ядро СУБД Microsoft Jet, и модуль Jet требует, чтобы приложение не начинало транзакцию в любой базе данных с открытым курсором. Для классов базы данных MFC ODBC открытый курсор эквивалентен открытому `CRecordset` объекту.

Если набор записей открывается перед вызовом `BeginTrans` , то могут не отображаться сообщения об ошибках. Однако при любом обновлении набора записей приложение становится постоянным после вызова `CRecordset::Update` , а обновления не будут отменены путем вызова `Rollback` . Чтобы избежать этой проблемы, необходимо сначала вызвать, `BeginTrans` а затем открыть набор записей.

MFC проверяет функциональность драйвера для фиксации и отката курсора. Класс `CDatabase` предоставляет две функции члена, `GetCursorCommitBehavior` и `GetCursorRollbackBehavior` , чтобы определить воздействие любой транзакции на открытый `CRecordset` объект. Для драйвера ODBC для Microsoft Access 7,0 эти функции-члены возвращают, `SQL_CB_CLOSE` так как драйвер доступа не поддерживает сохранение курсора. Поэтому необходимо вызвать `CRecordset::Requery` следующую `CommitTrans` `Rollback` операцию или.

Если необходимо выполнить несколько транзакций один за другим, нельзя вызвать `Requery` после первой транзакции, а затем запустить следующую. Чтобы удовлетворить требованиям Jet, необходимо закрыть набор записей до следующего вызова в `BeginTrans` . В этом техническом примечании описаны два метода обработки такой ситуации:

- Закрытие набора записей после каждой `CommitTrans` `Rollback` операции или.

- Использование функции ODBC API `SQLFreeStmt` .

## <a name="closing-the-recordset-after-each-committrans-or-rollback-operation"></a>Закрытие набора записей после каждой операции CommitTrans или ROLLBACK

Перед запуском транзакции убедитесь, что объект набора записей закрыт. После вызова `BeginTrans` вызовите `Open` функцию члена набора записей. Закройте набор записей сразу после вызова метода `CommitTrans` или `Rollback` . Обратите внимание, что многократное открытие и закрытие набора записей может снизить производительность приложения.

## <a name="using-sqlfreestmt"></a>Использование SQLFreeStmt

Можно также использовать функцию ODBC API `SQLFreeStmt` для явного закрытия курсора после завершения транзакции. Чтобы запустить другую транзакцию, вызовите вызов, `BeginTrans` за которым следует `CRecordset::Requery` . При вызове `SQLFreeStmt` необходимо указать хстмт набора записей в качестве первого параметра и *SQL_CLOSE* в качестве второго параметра. Этот метод выполняется быстрее, чем закрытие и открытие набора записей в начале каждой транзакции. В следующем коде показано, как реализовать этот метод:

```cpp
CMyDatabase db;
db.Open("MYDATASOURCE");
CMyRecordset rs(&db);

// start transaction 1 and
// open the recordset
db.BeginTrans();
rs.Open();

// manipulate data

// end transaction 1
db.CommitTrans(); // or Rollback()

// close the cursor
::SQLFreeStmt(rs.m_hstmt, SQL_CLOSE);

// start transaction 2
db.BeginTrans();
// now get the result set
rs.Requery();

// manipulate data

// end transaction 2
db.CommitTrans();

rs.Close();
db.Close();
```

Другим способом реализации этой методики является написание новой функции, `RequeryWithBeginTrans` которую можно вызвать для запуска следующей транзакции после фиксации или отката первой. Чтобы написать такую функцию, выполните следующие действия.

1. Скопируйте код `CRecordset::Requery( )` в новую функцию.

2. Добавьте следующую строку сразу после вызова `SQLFreeStmt` :

   `m_pDatabase->BeginTrans( );`

Теперь эту функцию можно вызывать между каждой парой транзакций:

```cpp
// start transaction 1 and
// open the recordset
db.BeginTrans();

rs.Open();

// manipulate data

// end transaction 1
db.CommitTrans();   // or Rollback()

// close the cursor, start new transaction,
// and get the result set
rs.RequeryWithBeginTrans();

// manipulate data

// end transaction 2
db.CommitTrans();   // or Rollback()
```

> [!NOTE]
> Не используйте этот метод, если необходимо изменить переменные члена набора записей *m_strFilter* или *m_strSort* между транзакциями. В этом случае необходимо закрыть набор записей после каждой `CommitTrans` `Rollback` операции или.

## <a name="see-also"></a>См. также раздел

[Технические примечания по номеру](../mfc/technical-notes-by-number.md)<br/>
[Технические примечания по категориям](../mfc/technical-notes-by-category.md)
