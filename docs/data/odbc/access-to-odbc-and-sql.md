---
description: Дополнительные сведения см. в статье доступ к ODBC и SQL.
title: Доступ к ODBC и SQL
ms.date: 11/04/2016
helpviewer_keywords:
- API calls [C++], calling DAO or ODBC directly
- Windows API [C++], calling from MFC
- ODBC API functions [C++]
- ODBC API functions [C++], calling from MFC
- SQL [C++], calling ODBC API functions
- ODBC [C++], API functions
ms.assetid: 5613d7dc-00b7-4646-99ae-1116c05c52b4
ms.openlocfilehash: 507e3a8e2d88c253f193de41be1a28ae0c5cba87
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97295150"
---
# <a name="access-to-odbc-and-sql"></a>Доступ к ODBC и SQL

Библиотека Microsoft Foundation Class инкапсулирует множество вызовов API Windows и по-прежнему позволяет напрямую вызывать любую функцию Windows API. Классы баз данных обеспечивают ту же гибкость, что и API ODBC. Хотя классы базы данных защищают от большей части сложности ODBC, вы можете вызывать функции API ODBC непосредственно из любого места в программе.

Аналогичным образом, классы базы данных защищают от необходимости работы с [SQL](../../data/odbc/sql.md), но вы можете использовать SQL напрямую, если хотите. Объекты набора записей можно настроить, передав пользовательскую инструкцию SQL (или настроив части инструкции по умолчанию) при открытии набора записей. Также можно выполнять вызовы SQL непосредственно с помощью функции члена [ExecuteSQL](../../mfc/reference/cdatabase-class.md#executesql) класса [CDatabase](../../mfc/reference/cdatabase-class.md).

Дополнительные сведения см. в разделе [ODBC: вызов функций API ODBC напрямую](../../data/odbc/odbc-calling-odbc-api-functions-directly.md) и [SQL: выполнение прямых вызовов SQL (ODBC)](../../data/odbc/sql-making-direct-sql-calls-odbc.md).

## <a name="see-also"></a>См. также раздел

[ODBC и MFC](../../data/odbc/odbc-and-mfc.md)
