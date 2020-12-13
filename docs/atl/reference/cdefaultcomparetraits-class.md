---
description: 'Дополнительные сведения о: Кдефаулткомпаретраитс Class'
title: Класс Кдефаулткомпаретраитс
ms.date: 11/04/2016
f1_keywords:
- CDefaultCompareTraits
- ATLCOLL/ATL::CDefaultCompareTraits
- ATLCOLL/ATL::CDefaultCompareTraits::CompareElements
- ATLCOLL/ATL::CDefaultCompareTraits::CompareElementsOrdered
helpviewer_keywords:
- CDefaultCompareTraits class
ms.assetid: a17e2740-e7b4-48f2-aeb7-c80ce84b63f7
ms.openlocfilehash: dcb366cdcd99a6eed2b641be290ccc4913a81476
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97141912"
---
# <a name="cdefaultcomparetraits-class"></a>Класс Кдефаулткомпаретраитс

Этот класс предоставляет функции сравнения элементов по умолчанию.

## <a name="syntax"></a>Синтаксис

```
template<typename T>
class CDefaultCompareTraits
```

#### <a name="parameters"></a>Параметры

*T*<br/>
Тип данных, сохраняемых в коллекции.

## <a name="members"></a>Элементы

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кдефаулткомпаретраитс:: Компарилементс](#compareelements)|Статически Вызовите эту функцию, чтобы сравнить два элемента на равенство.|
|[Кдефаулткомпаретраитс:: Компарилементсордеред](#compareelementsordered)|Статически Вызовите эту функцию для определения большего и меньшего элемента.|

## <a name="remarks"></a>Комментарии

Этот класс содержит две статические функции для сравнения элементов, хранящихся в объекте класса коллекции. Этот класс используется [классом кдефаултелементтраитс](../../atl/reference/cdefaultelementtraits-class.md).

Дополнительные сведения см. в разделе [классы коллекций ATL](../../atl/atl-collection-classes.md).

## <a name="requirements"></a>Требования

**Заголовок:** атлколл. h

## <a name="cdefaultcomparetraitscompareelements"></a><a name="compareelements"></a> Кдефаулткомпаретраитс:: Компарилементс

Вызовите эту функцию, чтобы сравнить два элемента на равенство.

```
static bool CompareElements(const T& element1, const T& element2);
```

### <a name="parameters"></a>Параметры

*Element1*<br/>
Первый элемент

*element2*<br/>
Второй элемент.

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение true, если элементы равны, и false в противном случае.

### <a name="remarks"></a>Комментарии

Реализацией по умолчанию этой функции является оператор равенства ( **==** ). Для объектов, отличных от простых типов данных, эту функцию может потребоваться переопределить.

## <a name="cdefaultcomparetraitscompareelementsordered"></a><a name="compareelementsordered"></a> Кдефаулткомпаретраитс:: Компарилементсордеред

Вызовите эту функцию для определения большего и меньшего элемента.

```
static int CompareElementsOrdered(const T& element1, const T& element2);
```

### <a name="parameters"></a>Параметры

*Element1*<br/>
Первый элемент

*element2*<br/>
Второй элемент.

### <a name="return-value"></a>Возвращаемое значение

Возвращает целое число, основанное на следующей таблице:

|Условие|Возвращаемое значение|
|---------------|------------------|
|*Element1*  <  *ELEMENT2*|<0|
|*Element1*  ==  *ELEMENT2*|0|
|*Element1*  >  *ELEMENT2*|> 0|

### <a name="remarks"></a>Комментарии

Реализация по умолчанию этой функции использует **==** операторы, **\<**, and **>** . Для объектов, отличных от простых типов данных, эту функцию может потребоваться переопределить.

## <a name="see-also"></a>См. также раздел

[Общие сведения о классах](../../atl/atl-class-overview.md)
