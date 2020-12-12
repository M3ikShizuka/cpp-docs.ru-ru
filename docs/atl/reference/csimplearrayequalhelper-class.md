---
description: 'Дополнительные сведения о: Ксимплеаррайекуалхелпер Class'
title: Класс Ксимплеаррайекуалхелпер
ms.date: 11/04/2016
f1_keywords:
- CSimpleArrayEqualHelper
- ATLSIMPCOLL/ATL::CSimpleArrayEqualHelper
- ATLSIMPCOLL/ATL::CSimpleArrayEqualHelper::IsEqual
helpviewer_keywords:
- CSimpleArrayEqualHelper class
ms.assetid: a2b55d89-78c9-42ef-842c-5304c6d20ad6
ms.openlocfilehash: e1a5fd3eea5fd6ef7563febc662c5a7a1bc639c5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97140768"
---
# <a name="csimplearrayequalhelper-class"></a>Класс Ксимплеаррайекуалхелпер

Этот класс является вспомогательным классом для класса [ксимплеаррай](../../atl/reference/csimplearray-class.md) .

## <a name="syntax"></a>Синтаксис

```
template <class T>
class CSimpleArrayEqualHelper
```

#### <a name="parameters"></a>Параметры

*T*<br/>
Производный класс.

## <a name="members"></a>Элементы

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Ксимплеаррайекуалхелпер:: Equals](#isequal)|Статически Проверяет два `CSimpleArray` объектных элемента на равенство.|

## <a name="remarks"></a>Комментарии

Этот класс признаков является дополнением к `CSimpleArray` классу. Он предоставляет метод для сравнения двух элементов, хранящихся в `CSimpleArray` объекте. По умолчанию элементы сравниваются с помощью **оператора operator = ()**, но если массив содержит сложные типы данных, у которых отсутствует собственный оператор равенства, необходимо переопределить этот класс.

## <a name="requirements"></a>Требования

**Заголовок:** атлсимпколл. h

## <a name="csimplearrayequalhelperisequal"></a><a name="isequal"></a> Ксимплеаррайекуалхелпер:: Equals

Проверяет два `CSimpleArray` объектных элемента на равенство.

```
static bool IsEqual(
    const T& t1,
    const T& t2);
```

### <a name="parameters"></a>Параметры

*T1*<br/>
Объект типа T.

*T2*<br/>
Объект типа T.

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение true, если элементы равны, и false в противном случае.

## <a name="see-also"></a>См. также раздел

[Класс Ксимплеаррай](../../atl/reference/csimplearray-class.md)<br/>
[Класс Ксимплеаррайекуалхелперфалсе](../../atl/reference/csimplearrayequalhelperfalse-class.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
