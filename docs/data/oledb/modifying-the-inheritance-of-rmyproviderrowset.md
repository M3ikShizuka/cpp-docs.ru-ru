---
description: 'Дополнительные сведения: изменение наследования Ркустомровсет'
title: Изменение наследования Ркустомровсет
ms.date: 10/26/2018
helpviewer_keywords:
- RMyProviderRowset
- inheritance [C++]
- RCustomRowset
ms.assetid: 33089c90-98a4-43e7-8e67-d4bb137e267e
ms.openlocfilehash: c54533122083c526ad12ac6514efa3ad9ba47cf5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97287012"
---
# <a name="modifying-the-inheritance-of-rcustomrowset"></a>Изменение наследования Ркустомровсет

Чтобы добавить `IRowsetLocate` интерфейс в простой пример поставщика, доступного только для чтения, измените наследование `CCustomRowset` . Изначально `CCustomRowset` наследует от `CRowsetImpl` . Его необходимо изменить, чтобы он наследовался от `CRowsetBaseImpl` .

Для этого создайте новый класс `CCustomRowsetImpl` в *пользовательском* RS. h:

```cpp
////////////////////////////////////////////////////////////////////////
// CustomRS.h

template <class T, class Storage, class CreatorClass, class ArrayType = CAtlArray<Storage>>
class CMyRowsetImpl:
   public CRowsetImpl<T, Storage, CreatorClass, ArrayType, CSimpleRow, IRowsetLocateImpl< T, IRowsetLocate >>
{
...
};
```

Теперь измените карту COM-интерфейсов в *пользовательском* RS. h следующим образом:

```cpp
BEGIN_COM_MAP(CMyRowsetImpl)
   COM_INTERFACE_ENTRY(IRowsetLocate)
   COM_INTERFACE_ENTRY_CHAIN(_RowsetBaseClass)
END_COM_MAP()
```

Этот код создает карту COM-интерфейса, которая сообщает о `CMyRowsetImpl` вызове `QueryInterface` для `IRowset` `IRowsetLocate` интерфейсов и. Чтобы получить всю реализацию для других классов наборов строк, Map связывает `CMyRowsetImpl` класс с `CRowsetBaseImpl` классом, определенным в шаблонах OLE DB; на карте используется макрос COM_INTERFACE_ENTRY_CHAIN, который сообщает OLE DB шаблонам сканировать карту com в `CRowsetBaseImpl` в ответ на `QueryInterface` вызов.

Наконец, свяжите `CCustomRowset` с `CMyRowsetBaseImpl` , изменив `CCustomRowset` для наследования `CMyRowsetImpl` , следующим образом:

```cpp
class CCustomRowset : public CMyRowsetImpl<CCustomRowset, CCustomWindowsFile, CCustomCommand>
```

`CCustomRowset` теперь может использовать `IRowsetLocate` интерфейс, используя преимущества остальной части реализации класса набора строк.

Когда это будет сделано, можно [динамически определить столбцы, возвращаемые потребителю](../../data/oledb/dynamically-determining-columns-returned-to-the-consumer.md).

## <a name="see-also"></a>См. также раздел

[Усовершенствование простого поставщика Read-Only](../../data/oledb/enhancing-the-simple-read-only-provider.md)<br/>
