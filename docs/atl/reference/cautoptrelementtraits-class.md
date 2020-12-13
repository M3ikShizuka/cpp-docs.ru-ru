---
description: 'Дополнительные сведения о: Каутоптрелементтраитс Class'
title: Класс Каутоптрелементтраитс
ms.date: 11/04/2016
f1_keywords:
- CAutoPtrElementTraits
- ATLCOLL/ATL::CAutoPtrElementTraits
- ATLCOLL/ATL::CAutoPtrElementTraits::INARGTYPE
- ATLCOLL/ATL::CAutoPtrElementTraits::OUTARGTYPE
helpviewer_keywords:
- CAutoPtrElementTraits class
ms.assetid: 777c1b14-6ab7-491f-b9a5-be149e71d4a2
ms.openlocfilehash: 2478f8251f0094aaa5cabf1c0dcc873c9c526cd8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97147138"
---
# <a name="cautoptrelementtraits-class"></a>Класс Каутоптрелементтраитс

Этот класс предоставляет методы, статические функции и определения типов, полезные при создании коллекций смарт-указателей.

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```
template<typename T>
class CAutoPtrElementTraits
    : public CDefaultElementTraits<ATL::CAutoPtr<T>>
```

#### <a name="parameters"></a>Параметры

*T*<br/>
Тип указателя.

## <a name="members"></a>Элементы

### <a name="public-typedefs"></a>Общедоступные определения типов

|Имя|Описание|
|----------|-----------------|
|[Каутоптрелементтраитс:: ИНАРГТИПЕ](#inargtype)|Тип данных, используемый для добавления элементов в объект класса коллекции.|
|[Каутоптрелементтраитс:: АУТАРГТИПЕ](#outargtype)|Тип данных, используемый для извлечения элементов из объекта класса коллекции.|

## <a name="remarks"></a>Комментарии

Этот класс предоставляет методы, статические функции и определения типов для использования при создании объектов класса коллекций, содержащих смарт-указатели. Классы [каутоптраррай](../../atl/reference/cautoptrarray-class.md) и [каутоптрлист](../../atl/reference/cautoptrlist-class.md) являются производными от `CAutoPtrElementTraits` . При построении коллекции смарт-указателей, для которых требуются операторы создания и удаления Vector, следует использовать [каутовекторптрелементтраитс](../../atl/reference/cautovectorptrelementtraits-class.md) .

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[кдефаулткомпаретраитс](../../atl/reference/cdefaultcomparetraits-class.md)

[кдефаулсаштраитс](../../atl/reference/cdefaulthashtraits-class.md)

[целементтраитсбасе](../../atl/reference/celementtraitsbase-class.md)

[кдефаултелементтраитс](../../atl/reference/cdefaultelementtraits-class.md)

`CAutoPtrElementTraits`

## <a name="requirements"></a>Требования

**Заголовок:** атлколл. h

## <a name="cautoptrelementtraitsinargtype"></a><a name="inargtype"></a> Каутоптрелементтраитс:: ИНАРГТИПЕ

Тип данных, используемый для добавления элементов в объект класса коллекции.

```
typedef CAutoPtr<T>& INARGTYPE;
```

## <a name="cautoptrelementtraitsoutargtype"></a><a name="outargtype"></a> Каутоптрелементтраитс:: АУТАРГТИПЕ

Тип данных, используемый для извлечения элементов из объекта класса коллекции.

```
typedef T *& OUTARGTYPE;
```

## <a name="see-also"></a>См. также раздел

[Класс Кдефаултелементтраитс](../../atl/reference/cdefaultelementtraits-class.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
