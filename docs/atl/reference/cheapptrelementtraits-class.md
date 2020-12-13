---
description: 'Дополнительные сведения о: Чеапптрелементтраитс Class'
title: Класс Чеапптрелементтраитс
ms.date: 11/04/2016
f1_keywords:
- CHeapPtrElementTraits
- ATLCOLL/ATL::CHeapPtrElementTraits
- ATLCOLL/ATL::CHeapPtrElementTraits::INARGTYPE
- ATLCOLL/ATL::CHeapPtrElementTraits::OUTARGTYPE
helpviewer_keywords:
- CHeapPtrElementTraits class
ms.assetid: 910e0e06-3c8b-4242-bf00-b57eb74fbc77
ms.openlocfilehash: 7ca3d194a284f06e6b5baa0530cb49bc93d8510a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97141613"
---
# <a name="cheapptrelementtraits-class"></a>Класс Чеапптрелементтраитс

Этот класс предоставляет методы, статические функции и определения типов, которые полезны при создании коллекций указателей кучи.

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```
template<typename T, class Allocator = ATL::CCRTAllocator>
class CHeapPtrElementTraits :
   public CDefaultElementTraits<ATL::CHeapPtr<T, Allocator>>
```

#### <a name="parameters"></a>Параметры

*T*<br/>
Тип объекта, который должен храниться в классе коллекции.

*Выделен*<br/>
Используемый класс выделения памяти. Значение по умолчанию — [ккрталлокатор](../../atl/reference/ccrtallocator-class.md).

## <a name="members"></a>Элементы

### <a name="public-typedefs"></a>Общедоступные определения типов

|Имя|Описание|
|----------|-----------------|
|[Чеапптрелементтраитс:: ИНАРГТИПЕ](#inargtype)|Тип данных, используемый для добавления элементов в объект класса коллекции.|
|[Чеапптрелементтраитс:: АУТАРГТИПЕ](#outargtype)|Тип данных, используемый для извлечения элементов из объекта класса коллекции.|

## <a name="remarks"></a>Комментарии

Этот класс предоставляет методы, статические функции и определения типов для использования при создании объектов класса коллекции, содержащих указатели кучи. Класс `CHeapPtrList` является производным от `CHeapPtrElementTraits` .

Дополнительные сведения см. в разделе [классы коллекций ATL](../../atl/atl-collection-classes.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[кдефаулткомпаретраитс](../../atl/reference/cdefaultcomparetraits-class.md)

[кдефаулсаштраитс](../../atl/reference/cdefaulthashtraits-class.md)

[целементтраитсбасе](../../atl/reference/celementtraitsbase-class.md)

[кдефаултелементтраитс](../../atl/reference/cdefaultelementtraits-class.md)

`CHeapPtrElementTraits`

## <a name="requirements"></a>Требования

**Заголовок:** атлколл. h

## <a name="cheapptrelementtraitsinargtype"></a><a name="inargtype"></a> Чеапптрелементтраитс:: ИНАРГТИПЕ

Тип данных, используемый для добавления элементов в объект класса коллекции.

```
typedef CHeapPtr<T, Allocator>& INARGTYPE;
```

## <a name="cheapptrelementtraitsoutargtype"></a><a name="outargtype"></a> Чеапптрелементтраитс:: АУТАРГТИПЕ

Тип данных, используемый для извлечения элементов из объекта класса коллекции.

```
typedef T *& OUTARGTYPE;
```

## <a name="see-also"></a>См. также раздел

[Класс Кдефаултелементтраитс](../../atl/reference/cdefaultelementtraits-class.md)<br/>
[Класс Ккомхеапптр](../../atl/reference/ccomheapptr-class.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
