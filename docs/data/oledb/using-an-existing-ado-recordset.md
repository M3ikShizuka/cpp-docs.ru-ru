---
description: 'Дополнительные сведения о: использование существующего набора записей ADO'
title: Использование существующего набора записей ADO
ms.date: 11/04/2016
helpviewer_keywords:
- ADO recordsets [C++]
- OLE DB consumer templates, ADO recordsets
- recordsets [C++], using in OLE DB
ms.assetid: a9b1de8a-d379-49b1-a26e-578741e9f6a8
ms.openlocfilehash: 4b5c3b5f621f3cbdba6f2d42fd95436495a5661e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97160952"
---
# <a name="using-an-existing-ado-recordset"></a>Использование существующего набора записей ADO

Чтобы смешать OLE DB шаблоны потребителей и активные объекты данных (ADO), используйте ADO для открытия набора записей (соответствующего набору строк в шаблонах потребителя OLE DB). Если у вас есть набор записей, выполните следующие действия, чтобы подключиться к набору строк OLE DB.

1. Вызовите методы `QueryInterface` для `IRowset` `IAccessor` указателей и.

    ```cpp
    IRowset* lpRowset = NULL;
    IAccessor* lpAccessor = NULL;
    lpUnk->QueryInterface(IID_IRowset, (void**)&lpRowset);
    lpUnk->QueryInterface(IID_IAccessor, (void**)&lpAccessor);
    ```

    > [!NOTE]
    > *лпунк* указывает на `IUnknown` объект набора записей ADO.

1. Присоедините метод доступа и набор строк к соответствующим OLE DB классам шаблонов потребителей.

    ```cpp
    CRowset rs;
    CAccessor accessor;

    accessor.AddAccessorInfo(0ul);      // 0 is the ordinal of an ADO accessor
    rs.m_spRowset.Attach(lpRowset);      // use the Attach method of CComPtr<>
    rs.SetAccessor(accessor);
    ```

## <a name="see-also"></a>См. также раздел

[Использование методов доступа](../../data/oledb/using-accessors.md)
