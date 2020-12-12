---
description: 'Дополнительные сведения о: Ксимплемапекуалхелпер Class'
title: Класс Ксимплемапекуалхелпер
ms.date: 11/04/2016
f1_keywords:
- CSimpleMapEqualHelper
- ATLSIMPCOLL/ATL::CSimpleMapEqualHelper
- ATLSIMPCOLL/ATL::CSimpleMapEqualHelper::IsEqualKey
- ATLSIMPCOLL/ATL::CSimpleMapEqualHelper::IsEqualValue
helpviewer_keywords:
- CSimpleMapEqualHelper class
ms.assetid: 9bb2968a-d609-405c-8272-ff3b42df6164
ms.openlocfilehash: 2b8ff742bf24b6c6c4354cef652e3fc697ffb1d9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97140612"
---
# <a name="csimplemapequalhelper-class"></a>Класс Ксимплемапекуалхелпер

Этот класс является вспомогательным классом для класса [ксимплемап](../../atl/reference/csimplemap-class.md) .

## <a name="syntax"></a>Синтаксис

```
template <class TKey, class TVal>
class CSimpleMapEqualHelper
```

#### <a name="parameters"></a>Параметры

*TKey*<br/>
Элемент key.

*твал*<br/>
Элемент value.

## <a name="members"></a>Элементы

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Ксимплемапекуалхелпер:: Исекуалкэй](#isequalkey)|Статически Проверяет два ключа на равенство.|
|[Ксимплемапекуалхелпер:: Исекуалвалуе](#isequalvalue)|Статически Проверяет два значения на равенство.|

## <a name="remarks"></a>Комментарии

Этот класс признаков является дополнением к `CSimpleMap` классу. Он предоставляет методы для сравнения двух `CSimpleMap` объектных элементов (в частности, компонентов ключа и значения) на равенство. По умолчанию ключи и значения сравниваются с помощью **оператора operator = = ()**, но если на карте содержатся сложные типы данных, у которых нет собственного оператора равенства, этот класс можно переопределить, чтобы предоставить дополнительные необходимые функции.

## <a name="requirements"></a>Требования

**Заголовок:** атлсимпколл. h

## <a name="csimplemapequalhelperisequalkey"></a><a name="isequalkey"></a> Ксимплемапекуалхелпер:: Исекуалкэй

Проверяет два ключа на равенство.

```
static bool IsEqualKey(const TKey& k1, const TKey& k2);
```

### <a name="parameters"></a>Параметры

*k1*<br/>
Первый ключ.

*k2*<br/>
Второй ключ.

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение true, если ключи равны; в противном случае — значение false.

## <a name="csimplemapequalhelperisequalvalue"></a><a name="isequalvalue"></a> Ксимплемапекуалхелпер:: Исекуалвалуе

Проверяет два значения на равенство.

```
static bool IsEqualValue(const TVal& v1, const TVal& v2);
```

### <a name="parameters"></a>Параметры

*Версия 1*<br/>
Первое значение в вычитании.

*Версия 2*<br/>
Второе значение в вычитании.

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение true, если значения равны, и false в противном случае.

## <a name="see-also"></a>См. также раздел

[Класс Ксимплемапекуалхелперфалсе](../../atl/reference/csimplemapequalhelperfalse-class.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
