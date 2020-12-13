---
description: 'Дополнительные сведения о: Целементтраитс Class'
title: Класс Целементтраитс
ms.date: 11/04/2016
f1_keywords:
- CElementTraits
- atlcoll/ATL::CElementTraits
helpviewer_keywords:
- CElementTraits class
ms.assetid: 496528e5-7f80-4b45-be0c-6f646feb43c5
ms.openlocfilehash: 1bcb6c9da2bca733efe68b634eebd7f379ba0d10
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97141808"
---
# <a name="celementtraits-class"></a>Класс Целементтраитс

Этот класс используется классами коллекций для предоставления методов и функций для операций перемещения, копирования, сравнения и хэширования.

## <a name="syntax"></a>Синтаксис

```
template<typename T>
class CElementTraits : public CDefaultElementTraits<T>
```

#### <a name="parameters"></a>Параметры

*T*<br/>
Тип данных, сохраняемых в коллекции.

## <a name="remarks"></a>Комментарии

Этот класс предоставляет статические функции и методы по умолчанию для перемещения, копирования, сравнения и хэширования элементов, хранящихся в объекте класса коллекции. `CElementTraits` указывается как поставщик по умолчанию для этих операций классами коллекций [CAtlArray](../../atl/reference/catlarray-class.md), [катллист](../../atl/reference/catllist-class.md), [крбмап](../../atl/reference/crbmap-class.md), [крбмултимап](../../atl/reference/crbmultimap-class.md)и [крбтри](../../atl/reference/crbtree-class.md).

Для простых типов данных достаточно реализаций по умолчанию, но если классы коллекций используются для хранения более сложных объектов, функции и методы должны быть переопределены реализациями, предоставляемыми пользователем.

Дополнительные сведения см. в разделе [классы коллекций ATL](../../atl/atl-collection-classes.md).

## <a name="requirements"></a>Требования

**Заголовок:** атлколл. h

## <a name="see-also"></a>См. также раздел

[Класс Кдефаултелементтраитс](../../atl/reference/cdefaultelementtraits-class.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
