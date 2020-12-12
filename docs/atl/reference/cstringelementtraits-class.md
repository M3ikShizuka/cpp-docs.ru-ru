---
description: 'Дополнительные сведения о: Кстринжелементтраитс Class'
title: Класс Кстринжелементтраитс
ms.date: 11/04/2016
f1_keywords:
- CStringElementTraits
- CSTRINGT/ATL::CStringElementTraits
- CSTRINGT/ATL::CStringElementTraits::INARGTYPE
- CSTRINGT/ATL::CStringElementTraits::OUTARGTYPE
- CSTRINGT/ATL::CStringElementTraits::CompareElements
- CSTRINGT/ATL::CStringElementTraits::CompareElementsOrdered
- CSTRINGT/ATL::CStringElementTraits::CopyElements
- CSTRINGT/ATL::CStringElementTraits::Hash
- CSTRINGT/ATL::CStringElementTraits::RelocateElements
helpviewer_keywords:
- CStringElementTraits class
ms.assetid: 74d7134b-099d-4455-bf91-3e68ccbf95bc
ms.openlocfilehash: 1e3f6a73e71530250d9dd88408165471028a18e9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97140495"
---
# <a name="cstringelementtraits-class"></a>Класс Кстринжелементтраитс

Этот класс предоставляет статические функции, используемые классами коллекций, в которых хранятся `CString` объекты.

## <a name="syntax"></a>Синтаксис

```
template <typename T>
class CStringElementTraits
```

#### <a name="parameters"></a>Параметры

*T*<br/>
Тип данных, сохраняемых в коллекции.

## <a name="members"></a>Элементы

### <a name="public-typedefs"></a>Общедоступные определения типов

|Имя|Описание|
|----------|-----------------|
|[Кстринжелементтраитс:: ИНАРГТИПЕ](#inargtype)|Тип данных, используемый для добавления элементов в объект класса коллекции.|
|[Кстринжелементтраитс:: АУТАРГТИПЕ](#outargtype)|Тип данных, используемый для извлечения элементов из объекта класса коллекции.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кстринжелементтраитс:: Компарилементс](#compareelements)|Статически Вызовите эту функцию, чтобы сравнить два строковых элемента на равенство.|
|[Кстринжелементтраитс:: Компарилементсордеред](#compareelementsordered)|Статически Вызовите эту функцию, чтобы сравнить два строковых элемента.|
|[Кстринжелементтраитс:: Копелементс](#copyelements)|Статически Вызывайте эту функцию для копирования `CString` элементов, хранящихся в объекте класса коллекции.|
|[Кстринжелементтраитс:: hash](#hash)|Статически Вызовите эту функцию, чтобы вычислить хэш-значение для заданного строкового элемента.|
|[Кстринжелементтраитс:: Релокатилементс](#relocateelements)|Статически Вызывайте эту функцию для перемещения `CString` элементов, хранящихся в объекте класса коллекции.|

## <a name="remarks"></a>Комментарии

Этот класс предоставляет статические функции для копирования, перемещения и сравнения строк, а также для создания хэш-значения. Эти функции полезны при использовании класса коллекции для хранения данных, основанных на строках. Используйте [кстринжелементтраитси](../../atl/reference/cstringelementtraitsi-class.md) , если требуются сравнения без учета регистра. Используйте [кстрингрефелементтраитс](../../atl/reference/cstringrefelementtraits-class.md) , если строковые объекты должны обрабатываться как ссылки.

Дополнительные сведения см. в разделе [классы коллекций ATL](../../atl/atl-collection-classes.md).

## <a name="requirements"></a>Требования

**Заголовок:** CStringT. h

## <a name="cstringelementtraitscompareelements"></a><a name="compareelements"></a> Кстринжелементтраитс:: Компарилементс

Вызовите эту статическую функцию, чтобы сравнить два строковых элемента на равенство.

```
static bool CompareElements(INARGTYPE str1, INARGTYPE str2);
```

### <a name="parameters"></a>Параметры

*str1*<br/>
Первый элемент строки.

*str2*<br/>
Второй строковый элемент.

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение true, если элементы равны, и false в противном случае.

## <a name="cstringelementtraitscompareelementsordered"></a><a name="compareelementsordered"></a> Кстринжелементтраитс:: Компарилементсордеред

Вызовите эту статическую функцию, чтобы сравнить два строковых элемента.

```
static int CompareElementsOrdered(INARGTYPE str1, INARGTYPE str2);
```

### <a name="parameters"></a>Параметры

*str1*<br/>
Первый элемент строки.

*str2*<br/>
Второй строковый элемент.

### <a name="return-value"></a>Возвращаемое значение

Нуль, если строки идентичны, < 0, если значение *str1* меньше *str2*, или > 0, если *str1* больше *str2*. Для выполнения сравнений используется метод [CStringT:: Compare](../../atl-mfc-shared/reference/cstringt-class.md#compare) .

## <a name="cstringelementtraitscopyelements"></a><a name="copyelements"></a> Кстринжелементтраитс:: Копелементс

Вызовите эту статическую функцию, чтобы скопировать `CString` элементы, хранящиеся в объекте класса коллекции.

```
static void CopyElements(
    T* pDest,
    const T* pSrc,
    size_t nElements);
```

### <a name="parameters"></a>Параметры

*pDest*<br/>
Указатель на первый элемент, который получит скопированные данные.

*pSrc*<br/>
Указатель на первый элемент для копирования.

*нелементс*<br/>
Число элементов для копирования.

### <a name="remarks"></a>Комментарии

Исходный и конечный элементы не должны перекрываться.

## <a name="cstringelementtraitshash"></a><a name="hash"></a> Кстринжелементтраитс:: hash

Вызовите эту статическую функцию, чтобы вычислить хэш-значение для заданного строкового элемента.

```
static ULONG Hash(INARGTYPE str);
```

### <a name="parameters"></a>Параметры

*str*<br/>
Строковый элемент.

### <a name="return-value"></a>Возвращаемое значение

Возвращает хэш-значение, вычисленное с использованием содержимого строки.

## <a name="cstringelementtraitsinargtype"></a><a name="inargtype"></a> Кстринжелементтраитс:: ИНАРГТИПЕ

Тип данных, используемый для добавления элементов в объект класса коллекции.

```
typedef T::PCXSTR INARGTYPE;
```

## <a name="cstringelementtraitsoutargtype"></a><a name="outargtype"></a> Кстринжелементтраитс:: АУТАРГТИПЕ

Тип данных, используемый для извлечения элементов из объекта класса коллекции.

```
typedef T& OUTARGTYPE;
```

## <a name="cstringelementtraitsrelocateelements"></a><a name="relocateelements"></a> Кстринжелементтраитс:: Релокатилементс

Вызовите эту статическую функцию для перемещения `CString` элементов, хранящихся в объекте класса коллекции.

```
static void RelocateElements(
    T* pDest,
    T* pSrc,
    size_t nElements);
```

### <a name="parameters"></a>Параметры

*pDest*<br/>
Указатель на первый элемент, который получит перемещенные данные.

*pSrc*<br/>
Указатель на первый элемент для перемещения.

*нелементс*<br/>
Число элементов для перемещения.

### <a name="remarks"></a>Комментарии

Эта статическая функция вызывает [memmove](../../c-runtime-library/reference/memmove-wmemmove.md), что достаточно для большинства типов данных. Если перемещаемые объекты содержат указатели на свои собственные члены, то эту статическую функцию необходимо переопределить.

## <a name="see-also"></a>См. также раздел

[Класс Целементтраитсбасе](../../atl/reference/celementtraitsbase-class.md)<br/>
[Класс Кстринжелементтраитси](../../atl/reference/cstringelementtraitsi-class.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
