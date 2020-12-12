---
description: 'Дополнительные сведения: OLE DB атрибуты потребителя'
title: OLE DB атрибуты потребителя (C++ COM)
ms.date: 10/02/2018
helpviewer_keywords:
- attributes [C++/CLI], database
- attributes [C++/CLI], data access
- databases [C++], attributes
- OLE DB consumers [C++], attributes
- database attributes [C++/CLI]
- attributes [C++/CLI], OLE DB consumer
ms.assetid: 017b591f-8f9a-42b4-84d5-cc42a21ab0cc
ms.openlocfilehash: bb974f29ee848477f025efbc6f7c0ccf6ee4f190
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97329714"
---
# <a name="ole-db-consumer-attributes"></a>Атрибуты потребителя OLE DB

OLE DB атрибуты потребителя вставляют код на основе [шаблонов OLE DB потребителей](../../data/oledb/ole-db-consumer-templates-reference.md), чтобы создать рабочий OLE DB потребитель, выполняющий такие задачи, как открытие таблиц, выполнение команд и доступ к данным.

|Атрибут|Описание|
|---------------|-----------------|
|[db_accessor](db-accessor.md)|Привязывает столбцы в наборе строк и привязывает их к соответствующим картам метода доступа.|
|[db_column](db-column.md)|Привязывает указанный столбец к набору строк.|
|[db_command](db-command.md)|Выполняет команду OLE DB.|
|[db_param](db-param.md)|Связывает указанную переменную элемента с входным или выходным параметром.|
|[db_source](db-source.md)|Создает и инкапсулирует соединение (через поставщика) к источнику данных.|
|[db_table](db-table.md)|Открывает таблицу OLE DB.|

## <a name="see-also"></a>См. также раздел

[Атрибуты по группам](attributes-by-group.md)
