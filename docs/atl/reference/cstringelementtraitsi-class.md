---
description: 'Дополнительные сведения о: Кстринжелементтраитси Class'
title: Класс Кстринжелементтраитси
ms.date: 11/04/2016
f1_keywords:
- CStringElementTraitsI
- ATLCOLL/ATL::CStringElementTraitsI
- ATLCOLL/ATL::CStringElementTraitsI::INARGTYPE
- ATLCOLL/ATL::CStringElementTraitsI::OUTARGTYPE
- ATLCOLL/ATL::CStringElementTraitsI::CompareElements
- ATLCOLL/ATL::CStringElementTraitsI::CompareElementsOrdered
- ATLCOLL/ATL::CStringElementTraitsI::Hash
helpviewer_keywords:
- CStringElementTraitsI class
ms.assetid: c23f92b1-91e5-400f-96ed-258b02622b7a
ms.openlocfilehash: 0a626677f4a62805933b2effb4811394626374a7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97140405"
---
# <a name="cstringelementtraitsi-class"></a>Класс Кстринжелементтраитси

Этот класс предоставляет статические функции, связанные со строками, хранящимися в объектах класса коллекции. Он аналогичен [кстринжелементтраитс](../../atl/reference/cstringelementtraits-class.md), но выполняет сравнения без учета регистра.

## <a name="syntax"></a>Синтаксис

```
template <typename T, class CharTraits = CDefaultCharTraits<T ::XCHAR>>
class CStringElementTraitsI : public CElementTraitsBase<T>
```

#### <a name="parameters"></a>Параметры

*T*<br/>
Тип данных, сохраняемых в коллекции.

## <a name="members"></a>Элементы

### <a name="public-typedefs"></a>Общедоступные определения типов

|Имя|Описание|
|----------|-----------------|
|[Кстринжелементтраитси:: ИНАРГТИПЕ](#inargtype)|Тип данных, используемый для добавления элементов в объект класса коллекции.|
|[Кстринжелементтраитси:: АУТАРГТИПЕ](#outargtype)|Тип данных, используемый для извлечения элементов из объекта класса коллекции.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кстринжелементтраитси:: Компарилементс](#compareelements)|Вызовите эту статическую функцию, чтобы сравнить два строковых элемента на равенство, игнорируя различия в регистре.|
|[Кстринжелементтраитси:: Компарилементсордеред](#compareelementsordered)|Вызовите эту статическую функцию, чтобы сравнить два строковых элемента, игнорируя различия в случае.|
|[Кстринжелементтраитси:: hash](#hash)|Вызовите эту статическую функцию, чтобы вычислить хэш-значение для заданного строкового элемента.|

## <a name="remarks"></a>Комментарии

Этот класс предоставляет статические функции для сравнения строк и создания хэш-значения. Эти функции полезны при использовании класса коллекции для хранения данных, основанных на строках. Используйте [кстрингрефелементтраитс](../../atl/reference/cstringrefelementtraits-class.md) , если строковые объекты должны быть обработаны как ссылки.

Дополнительные сведения см. в разделе [классы коллекций ATL](../../atl/atl-collection-classes.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[целементтраитсбасе](../../atl/reference/celementtraitsbase-class.md)

`CStringElementTraitsI`

## <a name="requirements"></a>Требования

**Заголовок:** атлколл. h

## <a name="cstringelementtraitsicompareelements"></a><a name="compareelements"></a> Кстринжелементтраитси:: Компарилементс

Вызовите эту статическую функцию, чтобы сравнить два строковых элемента на равенство, игнорируя различия в регистре.

```
static bool CompareElements(INARGTYPE str1, INARGTYPE str2) throw();
```

### <a name="parameters"></a>Параметры

*str1*<br/>
Первый элемент строки.

*str2*<br/>
Второй строковый элемент.

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение true, если элементы равны, и false в противном случае.

### <a name="remarks"></a>Комментарии

При сравнении регистр не учитывается.

## <a name="cstringelementtraitsicompareelementsordered"></a><a name="compareelementsordered"></a> Кстринжелементтраитси:: Компарилементсордеред

Вызовите эту статическую функцию, чтобы сравнить два строковых элемента, игнорируя различия в случае.

```
static int CompareElementsOrdered(INARGTYPE str1, INARGTYPE str2) throw();
```

### <a name="parameters"></a>Параметры

*str1*<br/>
Первый элемент строки.

*str2*<br/>
Второй строковый элемент.

### <a name="return-value"></a>Возвращаемое значение

Нуль, если строки идентичны, < 0, если значение *str1* меньше *str2*, или > 0, если *str1* больше *str2*. Для выполнения сравнений используется метод [CStringT:: Compare](../../atl-mfc-shared/reference/cstringt-class.md#compare) .

### <a name="remarks"></a>Комментарии

При сравнении регистр не учитывается.

## <a name="cstringelementtraitsihash"></a><a name="hash"></a> Кстринжелементтраитси:: hash

Вызовите эту статическую функцию, чтобы вычислить хэш-значение для заданного строкового элемента.

```
static ULONG Hash(INARGTYPE str) throw();
```

### <a name="parameters"></a>Параметры

*str*<br/>
Строковый элемент.

### <a name="return-value"></a>Возвращаемое значение

Возвращает хэш-значение, вычисленное с использованием содержимого строки.

## <a name="cstringelementtraitsiinargtype"></a><a name="inargtype"></a> Кстринжелементтраитси:: ИНАРГТИПЕ

Тип данных, используемый для добавления элементов в объект класса коллекции.

```
typedef T::PCXSTR INARGTYPE;
```

## <a name="cstringelementtraitsioutargtype"></a><a name="outargtype"></a> Кстринжелементтраитси:: АУТАРГТИПЕ

Тип данных, используемый для извлечения элементов из объекта класса коллекции.

```
typedef T& OUTARGTYPE;
```

## <a name="see-also"></a>См. также раздел

[Класс Целементтраитсбасе](../../atl/reference/celementtraitsbase-class.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)<br/>
[Класс Кстринжелементтраитс](../../atl/reference/cstringelementtraits-class.md)
