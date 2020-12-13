---
description: 'Дополнительные сведения о: Кпримитивилементтраитс Class'
title: Класс Кпримитивилементтраитс
ms.date: 11/04/2016
f1_keywords:
- CPrimitiveElementTraits
- ATLCOLL/ATL::CPrimitiveElementTraits
- ATLCOLL/ATL::CPrimitiveElementTraits::INARGTYPE
- ATLCOLL/ATL::CPrimitiveElementTraits::OUTARGTYPE
helpviewer_keywords:
- CPrimitiveElementTraits class
ms.assetid: 21c1cea8-2c5a-486c-b65c-85490f3ed4e6
ms.openlocfilehash: a9a47d9e6268ee6cc858d85e9236b00c270e8841
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97141080"
---
# <a name="cprimitiveelementtraits-class"></a>Класс Кпримитивилементтраитс

Этот класс предоставляет методы и функции по умолчанию для класса коллекции, состоящего из примитивных типов данных.

## <a name="syntax"></a>Синтаксис

```
template <typename T>
class CPrimitiveElementTraits : public CDefaultElementTraits<T>
```

#### <a name="parameters"></a>Параметры

*T*<br/>
Тип данных, сохраняемых в объекте класса коллекции.

## <a name="members"></a>Элементы

### <a name="public-typedefs"></a>Общедоступные определения типов

|Имя|Описание|
|----------|-----------------|
|[Кпримитивилементтраитс:: ИНАРГТИПЕ](#inargtype)|Тип данных, используемый для добавления элементов в объект класса коллекции.|
|[Кпримитивилементтраитс:: АУТАРГТИПЕ](#outargtype)|Тип данных, используемый для извлечения элементов из объекта класса коллекции.|

## <a name="remarks"></a>Комментарии

Этот класс предоставляет статические функции и методы по умолчанию для перемещения, копирования, сравнения и хэширования примитивных элементов типа данных, хранящихся в объекте класса коллекции.

Дополнительные сведения см. в разделе [классы коллекций ATL](../../atl/atl-collection-classes.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[кдефаулткомпаретраитс](../../atl/reference/cdefaultcomparetraits-class.md)

[кдефаулсаштраитс](../../atl/reference/cdefaulthashtraits-class.md)

[целементтраитсбасе](../../atl/reference/celementtraitsbase-class.md)

[кдефаултелементтраитс](../../atl/reference/cdefaultelementtraits-class.md)

`CPrimitiveElementTraits`

## <a name="requirements"></a>Требования

**Заголовок:** атлколл. h

## <a name="cprimitiveelementtraitsinargtype"></a><a name="inargtype"></a> Кпримитивилементтраитс:: ИНАРГТИПЕ

Тип данных, используемый для добавления элементов в объект класса коллекции.

```
typedef T INARGTYPE;
```

## <a name="cprimitiveelementtraitsoutargtype"></a><a name="outargtype"></a> Кпримитивилементтраитс:: АУТАРГТИПЕ

Тип данных, используемый для извлечения элементов из объекта класса коллекции.

```
typedef T& OUTARGTYPE;
```

## <a name="see-also"></a>См. также раздел

[Класс Кдефаултелементтраитс](../../atl/reference/cdefaultelementtraits-class.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
