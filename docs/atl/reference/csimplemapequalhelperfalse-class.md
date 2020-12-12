---
description: 'Дополнительные сведения о: Ксимплемапекуалхелперфалсе Class'
title: Класс Ксимплемапекуалхелперфалсе
ms.date: 11/04/2016
f1_keywords:
- CSimpleMapEqualHelperFalse
- ATLSIMPCOLL/ATL::CSimpleMapEqualHelperFalse
- ATLSIMPCOLL/ATL::CSimpleMapEqualHelperFalse::IsEqualKey
- ATLSIMPCOLL/ATL::CSimpleMapEqualHelperFalse::IsEqualValue
helpviewer_keywords:
- CSimpleMapEqualHelperFalse class
ms.assetid: a873eea3-e130-45cc-a476-61ee79511c3b
ms.openlocfilehash: 5bad8232dc1a96fc743a3526acdb86b839601d9a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97140586"
---
# <a name="csimplemapequalhelperfalse-class"></a>Класс Ксимплемапекуалхелперфалсе

Этот класс является вспомогательным классом для класса [ксимплемап](../../atl/reference/csimplemap-class.md) .

## <a name="syntax"></a>Синтаксис

```
template <class TKey, class TVal>
class CSimpleMapEqualHelperFalse
```

## <a name="members"></a>Члены

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Ксимплемапекуалхелперфалсе:: Исекуалкэй](#isequalkey)|Статически Проверяет два ключа на равенство.|
|[Ксимплемапекуалхелперфалсе:: Исекуалвалуе](#isequalvalue)|Статически Возвращает значение false.|

## <a name="remarks"></a>Комментарии

Этот класс признаков является дополнением к `CSimpleMap` классу. Он предоставляет метод для сравнения двух элементов, содержащихся в `CSimpleMap` объекте, в частности двух элементов значений или двух ключевых элементов.

При сравнении значений всегда будет возвращаться значение false, а в дополнение будет вызываться `ATLASSERT` с аргументом false, если ссылка на него возникает. В ситуациях, когда проверка на равенство не определена достаточно долго, этот класс позволяет карте, содержащей пары "ключ-значение", правильно работать для большинства методов, но не имеет четко определенного способа для методов, которые зависят от таких сравнений, как [ксимплемап:: финдвал](../../atl/reference/csimplemap-class.md#findval).

## <a name="requirements"></a>Требования

**Заголовок:** атлсимпколл. h

## <a name="csimplemapequalhelperfalseisequalkey"></a><a name="isequalkey"></a> Ксимплемапекуалхелперфалсе:: Исекуалкэй

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

### <a name="remarks"></a>Комментарии

Этот метод вызывает [ксимплеаррайекуалхелпер](../../atl/reference/csimplearrayequalhelper-class.md).

## <a name="csimplemapequalhelperfalseisequalvalue"></a><a name="isequalvalue"></a> Ксимплемапекуалхелперфалсе:: Исекуалвалуе

Возвращает значение false.

```
static bool IsEqualValue(const TVal&, const TVal&);
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение false.

### <a name="remarks"></a>Комментарии

Этот метод всегда возвращает значение false и будет вызываться `ATLASSERT` с аргументом false, если ссылка на него возникает. Целью `CSimpleMapEqualHelperFalse::IsEqualValue` является принудительное выполнение методов с использованием сравнений при сбое в четко определенном виде, когда проверки на равенство не определены надлежащим образом.

## <a name="see-also"></a>См. также раздел

[Класс Ксимплемапекуалхелпер](../../atl/reference/csimplemapequalhelper-class.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
