---
description: 'Дополнительные сведения о: Каутовекторптрелементтраитс Class'
title: Класс Каутовекторптрелементтраитс
ms.date: 11/04/2016
f1_keywords:
- CAutoVectorPtrElementTraits
- ATLCOLL/ATL::CAutoVectorPtrElementTraits
- ATLCOLL/ATL::CAutoVectorPtrElementTraits::INARGTYPE
- ATLCOLL/ATL::CAutoVectorPtrElementTraits::OUTARGTYPE
helpviewer_keywords:
- CAutoVectorPtrElementTraits class
ms.assetid: 16b81a56-55fb-46ca-b376-66a1884231a6
ms.openlocfilehash: 571b85c1b11968289d372f9c349ffcdb754dc381
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97147099"
---
# <a name="cautovectorptrelementtraits-class"></a>Класс Каутовекторптрелементтраитс

Этот класс предоставляет методы, статические функции и определения типов, полезные при создании коллекций смарт-указателей с помощью операторов Vector New и DELETE.

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```
template <typename T>
class CAutoVectorPtrElementTraits :
   public CDefaultElementTraits<ATL::CAutoVectorPtr<T>>
```

#### <a name="parameters"></a>Параметры

*T*<br/>
Тип указателя.

## <a name="members"></a>Элементы

### <a name="public-typedefs"></a>Общедоступные определения типов

|Имя|Описание|
|----------|-----------------|
|[Каутовекторптрелементтраитс:: ИНАРГТИПЕ](#inargtype)|Тип данных, используемый для добавления элементов в объект класса коллекции.|
|[Каутовекторптрелементтраитс:: АУТАРГТИПЕ](#outargtype)|Тип данных, используемый для извлечения элементов из объекта класса коллекции.|

## <a name="remarks"></a>Комментарии

Этот класс предоставляет методы, статические функции и определения типов для использования при создании объектов класса коллекций, содержащих смарт-указатели. В отличие от [каутоптрелементтраитс](../../atl/reference/cautoptrelementtraits-class.md), этот класс использует векторные операторы new и DELETE.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[кдефаулткомпаретраитс](../../atl/reference/cdefaultcomparetraits-class.md)

[кдефаулсаштраитс](../../atl/reference/cdefaulthashtraits-class.md)

[целементтраитсбасе](../../atl/reference/celementtraitsbase-class.md)

[кдефаултелементтраитс](../../atl/reference/cdefaultelementtraits-class.md)

`CAutoVectorPtrElementTraits`

## <a name="requirements"></a>Требования

**Заголовок:** атлколл. h

## <a name="cautovectorptrelementtraitsinargtype"></a><a name="inargtype"></a> Каутовекторптрелементтраитс:: ИНАРГТИПЕ

Тип данных, используемый для добавления элементов в объект класса коллекции.

```
typedef CAutoVectorPtr<T>& INARGTYPE;
```

## <a name="cautovectorptrelementtraitsoutargtype"></a><a name="outargtype"></a> Каутовекторптрелементтраитс:: АУТАРГТИПЕ

Тип данных, используемый для извлечения элементов из объекта класса коллекции.

```
typedef T*& OUTARGTYPE;
```

## <a name="see-also"></a>См. также раздел

[Класс Кдефаултелементтраитс](../../atl/reference/cdefaultelementtraits-class.md)<br/>
[Класс Каутовекторптр](../../atl/reference/cautovectorptr-class.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
