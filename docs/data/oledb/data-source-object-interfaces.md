---
description: Дополнительные сведения о интерфейсах объектов источника данных
title: Интерфейсы объекта источника данных
ms.date: 10/24/2018
helpviewer_keywords:
- data source objects [C++], interfaces
- data source objects [C++]
- interfaces [C++], OLE DB
- interfaces [C++], list of
- OLE DB provider templates [C++], object interfaces
- OLE DB [C++], interfaces
ms.assetid: 929e100c-c08c-4b64-8437-d8d1357226f6
ms.openlocfilehash: ecc37ca4286e288939ccd15bdcd073379c27f7c1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97287623"
---
# <a name="data-source-object-interfaces"></a>Интерфейсы объекта источника данных

В следующей таблице показаны обязательные и необязательные интерфейсы, определенные OLE DB для объекта источника данных.

|Интерфейс|Необходим?|Реализуется с помощью шаблонов OLE DB?|
|---------------|---------------|--------------------------------------|
|`IDBCreateSession`|Обязательный|Да|
|`IDBInitialize`|Обязательный|Да|
|`IDBProperties`|Обязательный|Да|
|[IPersist](/windows/win32/api/objidl/nn-objidl-ipersist)|Обязательный|Да|
|[IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer)|Необязательно|Нет|
|`IDBDataSourceAdmin`|Необязательно|Нет|
|`IDBInfo`|Необязательно|Нет|
|[IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile)|Необязательно|Нет|
|`ISupportErrorInfo`|Необязательно|Нет|

Объект источника данных реализует `IDBProperties` `IDBInitialize` интерфейсы, и `IDBCreateSession` посредством наследования. Можно выбрать поддержку дополнительных функций путем наследования или наследования от одного из этих классов реализации. Если требуется поддержка `IDBDataSourceAdmin` интерфейса, необходимо наследовать от `IDBDataSourceAdminImpl` класса.

## <a name="see-also"></a>См. также раздел

[Архитектура шаблона поставщика OLE DB](../../data/oledb/ole-db-provider-template-architecture.md)<br/>
