---
description: 'Дополнительные сведения о: Ккомкиптрелементтраитс Class'
title: Класс Ккомкиптрелементтраитс
ms.date: 11/04/2016
f1_keywords:
- CComQIPtrElementTraits
- ATLCOLL/ATL::CComQIPtrElementTraits
- ATLCOLL/ATL::CComQIPtrElementTraits::INARGTYPE
helpviewer_keywords:
- CComQIPtrElementTraits class
ms.assetid: 9df9250a-5413-4362-b133-332932a597c4
ms.openlocfilehash: 9aa96c5b926263d6ed58125a28f5d0a12d8107d3
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97142341"
---
# <a name="ccomqiptrelementtraits-class"></a>Класс Ккомкиптрелементтраитс

Этот класс предоставляет методы, статические функции и определения типов, полезные при создании коллекций указателей на COM-интерфейсах.

## <a name="syntax"></a>Синтаксис

```
template<typename I, const IID* piid=& __uuidof(I)>
class CComQIPtrElementTraits :
   public CDefaultElementTraits<ATL::CComQIPtr<I, piid>>
```

#### <a name="parameters"></a>Параметры

*I*<br/>
COM-интерфейс, указывающий тип сохраняемого указателя.

*пиид*<br/>
Указатель на идентификатор IID *I*.

## <a name="members"></a>Элементы

### <a name="public-typedefs"></a>Общедоступные определения типов

|Имя|Описание|
|----------|-----------------|
|[Ккомкиптрелементтраитс:: ИНАРГТИПЕ](#inargtype)|Тип данных, используемый для добавления элементов в объект класса коллекции.|

## <a name="remarks"></a>Комментарии

Этот класс наследует методы и предоставляет typedef, полезный при создании класса коллекции объектов указателя COM-интерфейса [CComQIPtr](../../atl/reference/ccomqiptr-class.md) . Этот класс используется как классами [Цинтерфацеаррай](../../atl/reference/cinterfacearray-class.md) , так и [Цинтерфацелист](../../atl/reference/cinterfacelist-class.md) .

Дополнительные сведения см. в разделе [классы коллекций ATL](../../atl/atl-collection-classes.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[кдефаулткомпаретраитс](../../atl/reference/cdefaultcomparetraits-class.md)

[кдефаулсаштраитс](../../atl/reference/cdefaulthashtraits-class.md)

[целементтраитсбасе](../../atl/reference/celementtraitsbase-class.md)

[кдефаултелементтраитс](../../atl/reference/cdefaultelementtraits-class.md)

`CComQIPtrElementTraits`

## <a name="requirements"></a>Требования

**Заголовок:** атлколл. h

## <a name="ccomqiptrelementtraitsinargtype"></a><a name="inargtype"></a> Ккомкиптрелементтраитс:: ИНАРГТИПЕ

Тип данных, используемый для добавления элементов в объект класса коллекции.

```
typedef I* INARGTYPE;
```

## <a name="see-also"></a>См. также раздел

[Класс Кдефаултелементтраитс](../../atl/reference/cdefaultelementtraits-class.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
