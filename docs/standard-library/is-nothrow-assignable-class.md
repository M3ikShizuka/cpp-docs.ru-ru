---
description: 'Дополнительные сведения о: is_nothrow_assignable классе'
title: Класс is_nothrow_assignable
ms.date: 11/04/2016
f1_keywords:
- type_traits/std::is_nothrow_assignable
helpviewer_keywords:
- is_nothrow_assignable
ms.assetid: aa3aca92-308b-4b1d-b3f3-c54216c48fe7
ms.openlocfilehash: 2d63c0f29b398cb8cd9eaef5e3e9e637c0b4eb16
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97230826"
---
# <a name="is_nothrow_assignable-class"></a>Класс is_nothrow_assignable

Проверяет, может ли значение *из* типа быть присвоено *типу,* и известно, что присваивание не вызывается.

## <a name="syntax"></a>Синтаксис

```cpp
template <class To, class From>
struct is_nothrow_assignable;
```

### <a name="parameters"></a>Параметры

*Кому*\
Тип объекта, который получает назначение.

*От*\
Тип объекта, который предоставляет значение.

## <a name="remarks"></a>Комментарии

Выражение `declval<To>() = declval<From>()` должно иметь правильный формат и быть известно компилятору как не вызывающее исключений. И *от* , и *до* должны быть полными типами, **`void`** или массивами с неизвестной границей.

## <a name="requirements"></a>Требования

**Заголовок:**\<type_traits>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[<type_traits>](../standard-library/type-traits.md)
