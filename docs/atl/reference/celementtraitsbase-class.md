---
description: 'Дополнительные сведения о: Целементтраитсбасе Class'
title: Класс Целементтраитсбасе
ms.date: 11/04/2016
f1_keywords:
- CElementTraitsBase
- ATLCOLL/ATL::CElementTraitsBase
- ATLCOLL/ATL::CElementTraitsBase::INARGTYPE
- ATLCOLL/ATL::CElementTraitsBase::OUTARGTYPE
- ATLCOLL/ATL::CElementTraitsBase::CopyElements
- ATLCOLL/ATL::CElementTraitsBase::RelocateElements
helpviewer_keywords:
- CElementTraitsBase class
ms.assetid: 75284caf-347e-4355-a7d8-efc708dd514a
ms.openlocfilehash: a200517e378cc3c3ca854ff60e9a49ac8e43d215
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97141782"
---
# <a name="celementtraitsbase-class"></a>Класс Целементтраитсбасе

Этот класс предоставляет методы копирования и перемещения по умолчанию для класса коллекции.

## <a name="syntax"></a>Синтаксис

```
template<typename T>
class CElementTraitsBase
```

#### <a name="parameters"></a>Параметры

*T*<br/>
Тип данных, сохраняемых в коллекции.

## <a name="members"></a>Элементы

### <a name="public-typedefs"></a>Общедоступные определения типов

|Имя|Описание|
|----------|-----------------|
|[Целементтраитсбасе:: ИНАРГТИПЕ](#inargtype)|Тип данных, используемый для добавления элементов в объект класса коллекции.|
|[Целементтраитсбасе:: АУТАРГТИПЕ](#outargtype)|Тип данных, используемый для извлечения элементов из объекта класса коллекции.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Целементтраитсбасе:: Копелементс](#copyelements)|Вызовите этот метод, чтобы скопировать элементы, хранящиеся в объекте класса коллекции.|
|[Целементтраитсбасе:: Релокатилементс](#relocateelements)|Вызовите этот метод, чтобы перенести элементы, хранящиеся в объекте класса коллекции.|

## <a name="remarks"></a>Комментарии

Этот базовый класс определяет методы для копирования и перемещения элементов в классе коллекции. Они используются классами [кдефаултелементтраитс](../../atl/reference/cdefaultelementtraits-class.md), [кстрингрефелементтраитс](../../atl/reference/cstringrefelementtraits-class.md)и [кстринжелементтраитси](../../atl/reference/cstringelementtraitsi-class.md).

Дополнительные сведения см. в разделе [классы коллекций ATL](../../atl/atl-collection-classes.md).

## <a name="requirements"></a>Требования

**Заголовок:** атлколл. h

## <a name="celementtraitsbasecopyelements"></a><a name="copyelements"></a> Целементтраитсбасе:: Копелементс

Вызовите этот метод, чтобы скопировать элементы, хранящиеся в объекте класса коллекции.

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

## <a name="celementtraitsbaseinargtype"></a><a name="inargtype"></a> Целементтраитсбасе:: ИНАРГТИПЕ

Тип данных, используемый для добавления элементов в коллекцию.

```
typedef const T& INARGTYPE;
```

## <a name="celementtraitsbaseoutargtype"></a><a name="outargtype"></a> Целементтраитсбасе:: АУТАРГТИПЕ

Тип данных, используемый для получения элементов из коллекции.

```
typedef T& OUTARGTYPE;
```

## <a name="celementtraitsbaserelocateelements"></a><a name="relocateelements"></a> Целементтраитсбасе:: Релокатилементс

Вызовите этот метод, чтобы перенести элементы, хранящиеся в объекте класса коллекции.

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

Этот метод вызывает [memmove](../../c-runtime-library/reference/memmove-wmemmove.md), который достаточно для большинства типов данных. Если перемещаемые объекты содержат указатели на свои собственные члены, этот метод потребуется переопределить.

## <a name="see-also"></a>См. также раздел

[Общие сведения о классах](../../atl/atl-class-overview.md)
