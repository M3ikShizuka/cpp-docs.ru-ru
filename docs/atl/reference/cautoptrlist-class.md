---
description: 'Дополнительные сведения о: Каутоптрлист Class'
title: Класс Каутоптрлист
ms.date: 11/04/2016
f1_keywords:
- CAutoPtrList
- ATLCOLL/ATL::CAutoPtrList
- ATLCOLL/ATL::CAutoPtrList::CAutoPtrList
helpviewer_keywords:
- CAutoPtrList class
ms.assetid: 11de4aca-28b0-4ff2-a74a-cb602312ffbd
ms.openlocfilehash: 51544d464904d0ebfd31b82152088a0dfa638969
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97152520"
---
# <a name="cautoptrlist-class"></a>Класс Каутоптрлист

Этот класс предоставляет методы, полезные при создании списка смарт-указателей.

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```
template<typename E>
class CAutoPtrList :
   public CAtlList<ATL::CAutoPtr<E>, CAutoPtrElementTraits<E>>
```

#### <a name="parameters"></a>Параметры

*E*<br/>
Тип указателя.

## <a name="members"></a>Элементы

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Каутоптрлист:: Каутоптрлист](#cautoptrlist)|Конструктор.|

## <a name="remarks"></a>Комментарии

Этот класс предоставляет конструктор и наследует методы от [катллист](../../atl/reference/catllist-class.md) и [каутоптрелементтраитс](../../atl/reference/cautoptrelementtraits-class.md) для облегчения создания объекта списка, в котором хранятся смарт-указатели. Класс [каутоптраррай](../../atl/reference/cautoptrarray-class.md) предоставляет аналогичную функцию для объекта массива.

Дополнительные сведения см. в разделе [классы коллекций ATL](../../atl/atl-collection-classes.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[катллист](../../atl/reference/catllist-class.md)

`CAutoPtrList`

## <a name="requirements"></a>Требования

**Заголовок:** атлколл. h

## <a name="cautoptrlistcautoptrlist"></a><a name="cautoptrlist"></a> Каутоптрлист:: Каутоптрлист

Конструктор.

```
CAutoPtrList(UINT nBlockSize = 10) throw();
```

### <a name="parameters"></a>Параметры

*нблокксизе*<br/>
Размер блока со значением по умолчанию 10.

### <a name="remarks"></a>Комментарии

Размер блока — это мера объема памяти, выделенной при необходимости нового элемента. Большие размеры блоков сокращают число вызовов подпрограмм выделения памяти, но используют больше ресурсов.

## <a name="see-also"></a>См. также раздел

[Класс Катллист](../../atl/reference/catllist-class.md)<br/>
[Класс Каутоптрелементтраитс](../../atl/reference/cautoptrelementtraits-class.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
