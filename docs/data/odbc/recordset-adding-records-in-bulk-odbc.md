---
description: 'Дополнительные сведения о: набор записей: создание записей в групповой операции (ODBC)'
title: Набор записей. Добавление нескольких записей (ODBC)
ms.date: 11/04/2016
helpviewer_keywords:
- ODBC recordsets, adding records
- recordsets, adding records
- bulk record additions to recordsets
ms.assetid: 4685f656-14b9-4f10-a1c5-147b2b89a0b4
ms.openlocfilehash: 5cb47fc8e96a38b2e5cc6c83cf464f28f2a85aaf
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97340402"
---
# <a name="recordset-adding-records-in-bulk-odbc"></a>Набор записей. Добавление нескольких записей (ODBC)

Этот раздел относится к классам ODBC библиотеки MFC.

Класс MFC [CRecordset](../../mfc/reference/crecordset-class.md) имеет новую оптимизацию, которая повышает эффективность при добавлении в таблицу новых записей.

> [!NOTE]
> Этот раздел относится к объектам, производным от `CRecordset`, в которых пакетное получение строк не реализовано. Если используется многострочная выборка строк, см. раздел [набор записей: групповая выборка записей (ODBC)](../../data/odbc/recordset-fetching-records-in-bulk-odbc.md).

Новый параметр для параметра *двоптионс* функции-члена [CRecordset:: Open](../../mfc/reference/crecordset-class.md#open) позволяет `optimizeBulkAdd` повысить производительность при последовательном добавлении нескольких записей без вызова метода `Requery` или `Close` . Только те поля, которые являются «грязными» до первого `Update` вызова, помечаются как «грязные» для последующих `AddNew` / `Update` вызовов.

Если вы используете классы базы данных, чтобы воспользоваться преимуществами `::SQLSetPos` функции ODBC API для добавления, изменения и удаления записей, такая оптимизация не требуется.

Если библиотека курсоров ODBC загружена или драйвер ODBC не поддерживает добавление, изменение и удаление с помощью `::SQLSetPos` , эта оптимизация повышает производительность при добавлении, изменении и удалении. Чтобы включить эту оптимизацию, задайте для параметра *двоптионс* в `Open` вызове набора записей следующее значение:

```
appendOnly | optimizeBulkAdd
```

## <a name="see-also"></a>См. также раздел

[Набор записей (ODBC)](../../data/odbc/recordset-odbc.md)<br/>
[Набор записей: Добавление, обновление и удаление записей (ODBC)](../../data/odbc/recordset-adding-updating-and-deleting-records-odbc.md)<br/>
[Набор записей. Блокировка записей (ODBC)](../../data/odbc/recordset-locking-records-odbc.md)
