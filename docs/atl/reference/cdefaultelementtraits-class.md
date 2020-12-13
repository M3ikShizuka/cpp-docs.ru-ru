---
description: 'Дополнительные сведения о: Кдефаултелементтраитс Class'
title: Класс Кдефаултелементтраитс
ms.date: 11/04/2016
f1_keywords:
- CDefaultElementTraits
- atlcoll/ATL::CDefaultElementTraits
helpviewer_keywords:
- CDefaultElementTraits class
ms.assetid: ac5ee610-7957-4b7c-92b6-38ff72e4118e
ms.openlocfilehash: f4dd1bae67ef626ef793ecee946d88879a07f194
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97141899"
---
# <a name="cdefaultelementtraits-class"></a>Класс Кдефаултелементтраитс

Этот класс предоставляет методы и функции по умолчанию для класса коллекции.

## <a name="syntax"></a>Синтаксис

```
template <typename T>
class CDefaultElementTraits : public CElementTraitsBase<T>,
    public CDefaultHashTraits<T>,
    public CDefaultCompareTraits<T>
```

#### <a name="parameters"></a>Параметры

*T*<br/>
Тип данных, сохраняемых в коллекции.

## <a name="remarks"></a>Комментарии

Этот класс предоставляет статические функции и методы по умолчанию для перемещения, копирования, сравнения и хэширования элементов, хранящихся в объекте класса коллекции. Этот класс наследует свои функции и методы от [целементтраитсбасе](../../atl/reference/celementtraitsbase-class.md), [кдефаулсаштраитс](../../atl/reference/cdefaulthashtraits-class.md)и [кдефаулткомпаретраитс](../../atl/reference/cdefaultcomparetraits-class.md)и используется [целементтраитс](../../atl/reference/celementtraits-class.md), [кпримитивилементтраитс](../../atl/reference/cprimitiveelementtraits-class.md)и [CHeapPtrElementTraits](../../atl/reference/cheapptrelementtraits-class.md).

Дополнительные сведения см. в разделе [классы коллекций ATL](../../atl/atl-collection-classes.md).

## <a name="requirements"></a>Требования

**Заголовок:** атлколл. h

## <a name="see-also"></a>См. также раздел

[Общие сведения о классах](../../atl/atl-class-overview.md)
