---
description: 'Дополнительные сведения о: Каутоптраррай Class'
title: Класс Каутоптраррай
ms.date: 11/04/2016
f1_keywords:
- CAutoPtrArray
- ATLCOLL/ATL::CAutoPtrArray
- ATLCOLL/ATL::CAutoPtrArray::CAutoPtrArray
helpviewer_keywords:
- CAutoPtrArray class
ms.assetid: 880a70da-8c81-4427-8ac6-49aa8d424244
ms.openlocfilehash: 55f9382c82a1e242342d0d740c369a571c43f9ba
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97152584"
---
# <a name="cautoptrarray-class"></a>Класс Каутоптраррай

Этот класс предоставляет методы, полезные при построении массива смарт-указателей.

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```cpp
template <typename E>
class CAutoPtrArray : public CAtlArray<
                        ATL::CAutoPtr<E>,
                        CAutoPtrElementTraits<E>>
```

### <a name="parameters"></a>Параметры

*E*<br/>
Тип указателя.

## <a name="members"></a>Элементы

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Каутоптраррай:: Каутоптраррай](#cautoptrarray)|Конструктор.|

## <a name="remarks"></a>Комментарии

Этот класс предоставляет конструктор и наследует методы от [CAtlArray](../../atl/reference/catlarray-class.md) и [каутоптрелементтраитс](../../atl/reference/cautoptrelementtraits-class.md) для облегчения создания объекта класса коллекции, в котором хранятся интеллектуальные указатели.

Дополнительные сведения см. в разделе [классы коллекций ATL](../../atl/atl-collection-classes.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`CAtlArray`

`CAutoPtrArray`

## <a name="requirements"></a>Требования

**Заголовок:** атлколл. h

## <a name="cautoptrarraycautoptrarray"></a><a name="cautoptrarray"></a> Каутоптраррай:: Каутоптраррай

Конструктор.

```cpp
CAutoPtrArray() throw();
```

### <a name="remarks"></a>Комментарии

Инициализирует массив интеллектуальных указателей.

## <a name="see-also"></a>См. также раздел

[Класс CAtlArray](../../atl/reference/catlarray-class.md)<br/>
[Класс Каутоптрелементтраитс](../../atl/reference/cautoptrelementtraits-class.md)<br/>
[Класс Каутоптрлист](../../atl/reference/cautoptrlist-class.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
