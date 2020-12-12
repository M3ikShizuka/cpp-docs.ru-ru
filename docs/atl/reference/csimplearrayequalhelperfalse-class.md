---
description: 'Дополнительные сведения о: Ксимплеаррайекуалхелперфалсе Class'
title: Класс Ксимплеаррайекуалхелперфалсе
ms.date: 11/04/2016
f1_keywords:
- CSimpleArrayEqualHelperFalse
- ATLSIMPCOLL/ATL::CSimpleArrayEqualHelperFalse
- ATLSIMPCOLL/ATL::CSimpleArrayEqualHelperFalse::IsEqual
helpviewer_keywords:
- CSimpleArrayEqualHelperFalse class
ms.assetid: 6918af6f-d23d-49eb-8482-c44272f5ffeb
ms.openlocfilehash: 196f7873f72799408a629bc784cb343966801d79
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97140729"
---
# <a name="csimplearrayequalhelperfalse-class"></a>Класс Ксимплеаррайекуалхелперфалсе

Этот класс является вспомогательным классом для класса [ксимплеаррай](../../atl/reference/csimplearray-class.md) .

## <a name="syntax"></a>Синтаксис

```
template <class T>
class CSimpleArrayEqualHelperFalse
```

#### <a name="parameters"></a>Параметры

*T*<br/>
Производный класс.

## <a name="members"></a>Элементы

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Ксимплеаррайекуалхелперфалсе:: Equals](#isequal)|Статически Возвращает значение false.|

## <a name="remarks"></a>Комментарии

Этот класс признаков является дополнением к `CSimpleArray` классу. Он всегда возвращает значение false и, Кроме того, будет вызывать `ATLASSERT` с аргументом false, если ссылка на него возникает. В ситуациях, когда проверка на равенство не определена достаточно, этот класс позволяет массиву, содержащему элементы, правильно работать для большинства методов, но в четко определенном порядке для методов, которые зависят от таких сравнений, как [ксимплеаррай:: Find](../../atl/reference/csimplearray-class.md#find).

## <a name="requirements"></a>Требования

**Заголовок:** атлсимпколл. h

## <a name="csimplearrayequalhelperfalseisequal"></a><a name="isequal"></a> Ксимплеаррайекуалхелперфалсе:: Equals

Возвращает значение false.

```
static bool IsEqual(const T&, const T&);
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение false.

### <a name="remarks"></a>Комментарии

Этот метод всегда возвращает значение false и будет вызывать `ATLASSERT` с аргументом false при ссылке. Целью `CSimpleArrayEqualHelperFalse::IsEqual` является принудительное выполнение методов с использованием сравнений при сбое в четко определенном виде, когда проверки на равенство не определены надлежащим образом.

## <a name="see-also"></a>См. также раздел

[Класс Ксимплеаррайекуалхелпер](../../atl/reference/csimplearrayequalhelper-class.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
