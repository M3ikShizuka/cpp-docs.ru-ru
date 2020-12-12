---
description: 'Дополнительные сведения: получение уведомлений'
title: Получение уведомлений
ms.date: 10/24/2018
helpviewer_keywords:
- notifications [C++], OLE DB consumers
- receiving notifications in OLE DB
- events [C++], notifications in OLE DB
- notifications [C++], events
- OLE DB consumers, notifications
- rowsets, event notifications
- OLE DB providers, notifications
ms.assetid: 305a1103-0c87-40c8-94bc-7fbbdd52ae32
ms.openlocfilehash: 1885223a7d2b3e932cf449312eab989ecf1d2554
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97316886"
---
# <a name="receiving-notifications"></a>Получение уведомлений

OLE DB предоставляет интерфейсы для получения уведомлений при возникновении событий. Они описаны в разделе [уведомления об объектах OLE DB](/previous-versions/windows/desktop/ms725406(v=vs.85)) в **справочнике по программированию OLE DB**. При установке этих событий используется стандартный механизм точки подключения COM. Например, объект ATL, который хочет получить события посредством `IRowsetNotify` `IRowsetNotify` , реализует интерфейс путем добавления `IRowsetNotify` в список, производный от класса, и предоставляет его через макрос COM_INTERFACE_ENTRY.

`IRowsetNotify` имеет три метода, которые могут быть вызваны в различные моменты времени. Если вы хотите ответить только на один из этих методов, можно использовать класс [IRowsetNotifyImpl](../../data/oledb/irowsetnotifyimpl-class.md) , который возвращает E_NOTIMPL для методов, которые вас не интересуют.

При создании набора строк необходимо сообщить поставщику, что должен поддерживаться возвращаемый объект набора строк `IConnectionPointContainer` , который необходим для настройки уведомления.

В следующем коде показано, как открыть набор строк из объекта ATL и использовать `AtlAdvise` функцию для настройки приемника уведомлений. `AtlAdvise` Возвращает файл cookie, который используется при вызове метода `AtlUnadvise` .

```cpp
CDBPropSet propset(DBPROPSET_ROWSET);
propset.AddProperty(DBPROP_IConnectionPointContainer, true);
```

Затем используется следующий код:

```cpp
product.Open(session, _T("Products"), &propset);

AtlAdvise(product.m_spRowset, GetUnknown(), IID_IRowsetNotify, &m_dwCookie);
```

## <a name="see-also"></a>См. также раздел

[Использование методов доступа](../../data/oledb/using-accessors.md)
