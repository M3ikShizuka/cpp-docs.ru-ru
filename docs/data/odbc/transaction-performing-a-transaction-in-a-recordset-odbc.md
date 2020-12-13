---
description: 'Дополнительные сведения о транзакции: выполнение транзакции в наборе записей (ODBC)'
title: 'Транзакции: выполнение транзакции в наборе записей (ODBC)'
ms.date: 11/04/2016
helpviewer_keywords:
- transactions, updating recordsets
ms.assetid: cf1d6b48-7fb8-4903-84f7-a1822054534d
ms.openlocfilehash: bb041d35e7ab0bfc7e19f2658a8cdadae4bd8c7e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97333887"
---
# <a name="transaction-performing-a-transaction-in-a-recordset-odbc"></a>Транзакции: выполнение транзакции в наборе записей (ODBC)

В этом разделе объясняется, как выполнить транзакцию в наборе записей.

> [!NOTE]
> Поддерживается только один уровень транзакций; вложенные транзакции не допускают.

#### <a name="to-perform-a-transaction-in-a-recordset"></a>Выполнение транзакции в наборе записей

1. Вызовите `CDatabase` `BeginTrans` функцию члена объекта.

1. Если не реализована многострочная выборка строк, вызывайте `AddNew/Update` `Edit/Update` `Delete` функции элементов, и одного или нескольких объектов набора записей одной и той же базы данных столько раз, сколько необходимо. Дополнительные сведения см. в разделе [набор записей: Добавление, обновление и удаление записей (ODBC)](../../data/odbc/recordset-adding-updating-and-deleting-records-odbc.md). При реализации групповой выборки строк необходимо написать собственные функции для обновления источника данных.

1. Наконец, вызовите `CDatabase` `CommitTrans` функцию члена объекта. Если в одном из обновлений возникает ошибка или вы решили отменить изменения, вызовите ее `Rollback` функцию члена.

В следующем примере используются два набора записей для удаления регистрации учащегося из базы данных регистрации учебного заведения, удаление учащегося из всех классов, в которых зарегистрирован студент. Так как `Delete` вызовы в обоих наборах записей должны быть выполнены, требуется транзакция. В примере предполагается существование `m_dbStudentReg` , переменная-член типа, `CDatabase` уже подключенная к источнику данных, а также классы наборов записей `CEnrollmentSet` и `CStudentSet` . `strStudentID`Переменная содержит значение, полученное от пользователя.

```
BOOL CEnrollDoc::RemoveStudent( CString strStudentID )
{
    // remove student from all the classes
    // the student is enrolled in

    if ( !m_dbStudentReg.BeginTrans( ) )
        return FALSE;

    CEnrollmentSet rsEnrollmentSet(&m_dbStudentReg);
    rsEnrollmentSet.m_strFilter = "StudentID = " + strStudentID;

    if ( !rsEnrollmentSet.Open(CRecordset::dynaset) )
        return FALSE;

    CStudentSet rsStudentSet(&m_dbStudentReg);
    rsStudentSet.m_strFilter = "StudentID = " + strStudentID;

    if ( !rsStudentSet.Open(CRecordset::dynaset) )
        return FALSE;

    TRY
    {
        while ( !rsEnrollmentSet.IsEOF( ) )
        {
            rsEnrollmentSet.Delete( );
            rsEnrollmentSet.MoveNext( );
        }

        // delete the student record
        rsStudentSet.Delete( );

        m_dbStudentReg.CommitTrans( );
    }

    CATCH_ALL(e)
    {
        m_dbStudentReg.Rollback( );
        return FALSE;
    }
    END_CATCH_ALL

    rsEnrollmentSet.Close( );
    rsStudentSet.Close( );

    return TRUE;

}
```

> [!NOTE]
> `BeginTrans`Повторный вызов без вызова метода `CommitTrans` или `Rollback` является ошибкой.

## <a name="see-also"></a>См. также раздел

[Транзакция (ODBC)](../../data/odbc/transaction-odbc.md)<br/>
[Транзакция: влияние транзакций на обновления (ODBC)](../../data/odbc/transaction-how-transactions-affect-updates-odbc.md)<br/>
[Класс CDatabase](../../mfc/reference/cdatabase-class.md)<br/>
[Класс CRecordset](../../mfc/reference/crecordset-class.md)
