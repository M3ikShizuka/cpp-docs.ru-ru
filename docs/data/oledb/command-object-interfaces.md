---
description: 'Дополнительные сведения: интерфейсы объектов Command'
title: Интерфейсы объекта Command
ms.date: 10/24/2018
helpviewer_keywords:
- command object interfaces [C++]
- command objects [OLE DB]
- OLE DB [C++], command object interfaces
ms.assetid: dacff5ae-252c-4f20-9ad7-4e602cc48536
ms.openlocfilehash: 07dce6a71e7afd3a47c63942d48dd78d758103f8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97307526"
---
# <a name="command-object-interfaces"></a>Интерфейсы объекта Command

Объект Command использует `IAccessor` интерфейс для указания привязок параметров. Потребитель вызывает `IAccessor::CreateAccessor` , передавая ему массив `DBBINDING` структур. `DBBINDING` содержит сведения о привязках столбцов (например, тип и длина). Поставщик получает структуры и определяет способ передачи данных и необходимость преобразования.

`ICommandText`Интерфейс предоставляет способ указания текстовой команды. `ICommandProperties`Интерфейс обрабатывает все свойства команд.

## <a name="see-also"></a>См. также раздел

[Архитектура шаблона поставщика OLE DB](../../data/oledb/ole-db-provider-template-architecture.md)<br/>
