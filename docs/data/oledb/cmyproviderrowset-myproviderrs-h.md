---
description: 'Дополнительные сведения о: Ккустомровсет (Кустомрс. H)'
title: CCustomRowset (CustomRS.H)
ms.date: 10/22/2018
f1_keywords:
- cmyproviderrowset
- ccustomrowset
helpviewer_keywords:
- OLE DB providers, wizard-generated files
- CMyProviderRowset class in MyProviderRS.H
- CCustomRowset class in CustomRS.H
ms.assetid: 7ba1a124-3842-40eb-a36b-302190a1af3a
ms.openlocfilehash: 87025be2a34f8c850bde2be53ab01519968654d3
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97170468"
---
# <a name="ccustomrowset-customrsh"></a>CCustomRowset (CustomRS.H)

Мастер создает запись для объекта набора строк. В этом случае он называется `CCustomRowset` . `CCustomRowset`Класс наследует от класса поставщика OLE DB с именем `CRowsetImpl` , который реализует все необходимые интерфейсы для объекта набора строк. В следующем коде показана цепочка наследования для `CRowsetImpl` :

```cpp
template <class T, class Storage, class CreatorClass,
   class ArrayType = CAtlArray<Storage>>
class CMyRowsetImpl:
   public CRowsetImpl<T, Storage, CreatorClass, ArrayType,
      CSimpleRow, IRowsetLocateImpl< T >>
```

`CRowsetImpl` также использует `IAccessor` интерфейсы и `IColumnsInfo` . Он использует эти интерфейсы для выходных полей в таблицах. Класс также предоставляет реализацию для `IRowsetIdentity` , который позволяет потребителю определить, совпадают ли две строки. `IRowsetInfo`Интерфейс реализует свойства для объекта набора строк. `IConvertType`Интерфейс позволяет поставщику разрешать различия между типами данных, запрошенными потребителем, и теми, которые используются поставщиком.

`IRowset`Интерфейс фактически обрабатывает извлечение данных. Потребитель сначала вызывает метод, вызываемый `GetNextRows` для возврата маркера в строку, известный как `HROW` . Затем потребитель вызывает метод `IRowset::GetData` , `HROW` чтобы получить запрошенные данные.

`CRowsetImpl` также принимает несколько параметров шаблона. Эти параметры позволяют определить, как `CRowsetImpl` класс обрабатывает данные. `ArrayType`Аргумент позволяет определить, какой механизм хранения используется для хранения данных строки. Параметр *ровкласс* указывает, какой класс содержит `HROW` .

Параметр *ровсетинтерфаце* позволяет также использовать `IRowsetLocate` `IRowsetScroll` интерфейс или. `IRowsetLocate`Интерфейсы и `IRowsetScroll` наследуют от `IRowset` . Таким образом, шаблоны поставщика OLE DB должны обеспечивать специальную обработку этих интерфейсов. Если вы хотите использовать любой из этих интерфейсов, необходимо использовать этот параметр.

## <a name="see-also"></a>См. также раздел

[Файлы Wizard-Generated поставщика](../../data/oledb/provider-wizard-generated-files.md)<br/>
