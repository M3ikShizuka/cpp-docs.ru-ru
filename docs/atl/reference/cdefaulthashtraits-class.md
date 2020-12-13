---
description: 'Дополнительные сведения о: Кдефаулсаштраитс Class'
title: Класс Кдефаулсаштраитс
ms.date: 11/04/2016
f1_keywords:
- CDefaultHashTraits
- ATLCOLL/ATL::CDefaultHashTraits
- ATLCOLL/ATL::CDefaultHashTraits::Hash
helpviewer_keywords:
- CDefaultHashTraits class
ms.assetid: d8ec4b37-6d58-447b-a0c1-8580c5b1ab85
ms.openlocfilehash: 85cc881466be03931d435d91a48548456d74305b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97141886"
---
# <a name="cdefaulthashtraits-class"></a>Класс Кдефаулсаштраитс

Этот класс предоставляет статическую функцию для вычисления хэш-значений.

## <a name="syntax"></a>Синтаксис

```
template<typename T>
class CDefaultHashTraits
```

#### <a name="parameters"></a>Параметры

*T*<br/>
Тип данных, сохраняемых в коллекции.

## <a name="members"></a>Элементы

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кдефаулсаштраитс:: hash](#hash)|Статически Вызовите эту функцию, чтобы вычислить хэш-значение для заданного элемента.|

## <a name="remarks"></a>Комментарии

Этот класс содержит одну статическую функцию, которая возвращает хэш-значение для заданного элемента. Этот класс используется [классом кдефаултелементтраитс](../../atl/reference/cdefaultelementtraits-class.md).

Дополнительные сведения см. в разделе [классы коллекций ATL](../../atl/atl-collection-classes.md).

## <a name="requirements"></a>Требования

**Заголовок:** атлколл. h

## <a name="cdefaulthashtraitshash"></a><a name="hash"></a> Кдефаулсаштраитс:: hash

Вызовите эту функцию, чтобы вычислить хэш-значение для заданного элемента.

```
static ULONG Hash(const T& element) throw();
```

### <a name="parameters"></a>Параметры

*дерев*<br/>
Элемент.

### <a name="return-value"></a>Возвращаемое значение

Возвращает хэш-значение.

### <a name="remarks"></a>Комментарии

Алгоритм хэширования по умолчанию очень прост: возвращаемое значение является номером элемента. Переопределите эту функцию, если требуется более сложный алгоритм.

## <a name="see-also"></a>См. также раздел

[Общие сведения о классах](../../atl/atl-class-overview.md)
