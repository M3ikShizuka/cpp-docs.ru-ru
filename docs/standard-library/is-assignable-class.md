---
description: 'Дополнительные сведения о: is_assignable классе'
title: Класс is_assignable
ms.date: 11/04/2016
f1_keywords:
- type_traits/std::is_assignable
helpviewer_keywords:
- is_assignable
ms.assetid: 53444287-c8be-4ad2-9487-a85c066a4f84
ms.openlocfilehash: 4165e69de99b7fdb8ae1524d1755e738c846d7c0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97323864"
---
# <a name="is_assignable-class"></a>Класс is_assignable

Проверяет, можно ли назначить значение типа `From` типу `To`.

## <a name="syntax"></a>Синтаксис

```cpp
template <class To, class From>
struct is_assignable;
```

### <a name="parameters"></a>Параметры

*Кому*\
Тип объекта, который получает назначение.

*От*\
Тип объекта, который предоставляет значение.

## <a name="remarks"></a>Комментарии

Невычисленное выражение `declval<To>() = declval<From>()` должно иметь правильный формат. `From`И `To` должны быть полными типами, **`void`** или массивами с неизвестной границей.

## <a name="requirements"></a>Требования

**Заголовок:**\<type_traits>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[<type_traits>](../standard-library/type-traits.md)
