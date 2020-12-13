---
description: 'Дополнительные сведения: атрибуты элементов данных'
title: Атрибуты элементов данных (C++ COM)
ms.date: 10/02/2018
helpviewer_keywords:
- attributes [C++/CLI], reference topics
- data members [C++], attributes
- data members [C++]
ms.assetid: 95b2397d-1daf-4ae4-8cd0-06956d005b13
ms.openlocfilehash: 2bc5878b927ee8f80721928cdc6d9dbc3b095ea5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97333137"
---
# <a name="data-member-attributes"></a>Атрибуты членов данных

Следующие атрибуты применяются к элементам данных в классе, классе или интерфейсе.

|Атрибут|Описание|
|---------------|-----------------|
|[db_accessor](db-accessor.md)|Группирует `db_column` атрибуты, участвующие в `IAccessor` привязке на основе.|
|[db_column](db-column.md)|Привязывает указанный столбец к набору строк.|
|[db_command](db-command.md)|Создает команду OLE DB.|
|[db_param](db-param.md)|Связывает указанную переменную элемента с входным или выходным параметром и разделяет переменную.|
|[db_source](db-source.md)|Создает соединение с источником данных.|
|[db_table](db-table.md)|Открывает таблицу OLE DB.|
|[defaultbind](defaultbind.md)|Указывает отдельное, связываемое свойство, которое лучше соответствует объекту.|
|[displaybind](displaybind.md)|Указывает свойство, которое должно быть отображено пользователю как связываемое.|
|[id](id.md)|Указывает идентификатор DISPID для функции-члена (свойства или метода в интерфейсе или DISP).|
|[range](range-cpp.md)|Задает диапазон допустимых значений для аргументов или полей, значения которых задаются во время выполнения.|
|[RDX](rdx.md)|Создает раздел реестра или изменяет существующий раздел реестра.|
|[readonly](readonly-cpp.md)|Запрещает назначение элементу данных.|
|[requestedit](requestedit.md)|Указывает, что свойство поддерживает уведомление `OnRequestEdit`.|

## <a name="see-also"></a>См. также раздел

[Атрибуты по использованию](attributes-by-usage.md)
