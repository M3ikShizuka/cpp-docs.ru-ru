---
description: 'Дополнительные сведения о: источник данных: программное создание таблицы в источнике данных ODBC'
title: Программное создание таблицы в источнике данных ODBC
ms.date: 11/04/2016
helpviewer_keywords:
- programmatically creating ODBC tables [C++]
- tables [C++]
- ODBC data sources, creating tables in
- tables [C++], creating programmatically
ms.assetid: 9ca68fb5-c3df-424a-a75c-e3fb01cc1b18
ms.openlocfilehash: b195cc4fb81f1caed0b280c5df6a2032f4944ddf
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97155713"
---
# <a name="data-source-programmatically-creating-a-table-in-an-odbc-data-source"></a>Источник данных. Создание таблицы в источнике данных ODBC программным путем

В этом разделе объясняется, как создать таблицу для источника данных с помощью `ExecuteSQL` функции-члена класса `CDatabase` , передав функции строку, содержащую инструкцию SQL **CREATE TABLE** .

Общие сведения об источниках данных ODBC в MFC см. в разделе [Data Source (ODBC)](../../data/odbc/data-source-odbc.md). Раздел [источник данных. Программная настройка источника данных ODBC](../../data/odbc/data-source-programmatically-configuring-an-odbc-data-source.md) описывает создание источников данных.

Если источник данных установлен, можно легко создавать таблицы с помощью `ExecuteSQL` функции Member и инструкции SQL **CREATE TABLE** . Например, если `CDatabase` объект называется `myDB` , для создания таблицы можно использовать следующий код MFC:

```
myDB.ExecuteSQL("CREATE TABLE OFFICES (OfficeID TEXT(4)" ",
                         OfficeName TEXT(10))");
```

Этот пример кода создает таблицу с именем "офисы" в соединении с источником данных Microsoft Access, поддерживаемом `myDB` . в таблице содержатся два поля "оффицеид" и "оффиценаме".

> [!NOTE]
> Типы полей, указанные в инструкции SQL **CREATE TABLE** , могут различаться в зависимости от используемого драйвера ODBC. Программа Microsoft Query (распространяемая с Visual C++ 1,5) — это один из способов узнать, какие типы полей доступны для источника данных. В Microsoft Query выберите **файл**, щелкните **Table_Definition**, выберите таблицу из источника данных и посмотрите на тип, показанный в поле со списком **тип** . Для создания индексов также существует синтаксис SQL.

## <a name="see-also"></a>См. также раздел

[Источник данных (ODBC)](../../data/odbc/data-source-odbc.md)
