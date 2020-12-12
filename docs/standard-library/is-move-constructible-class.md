---
description: 'Дополнительные сведения о: is_move_constructible классе'
title: Класс is_move_constructible
ms.date: 10/24/2019
f1_keywords:
- type_traits/std::is_move_constructible
helpviewer_keywords:
- is_move_constructible
ms.assetid: becdf076-7419-488d-a335-78adf2478b9b
ms.openlocfilehash: 05ef640b2841eb3ab66f6d5a6d3b8ede7acf2754
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97323637"
---
# <a name="is_move_constructible-class"></a>Класс is_move_constructible

Проверяет, может ли тип быть создан с помощью операции перемещения.

## <a name="syntax"></a>Синтаксис

```cpp
template <class T>
struct is_move_constructible;
```

### <a name="parameters"></a>Параметры

*T*\
Оцениваемый тип.

## <a name="remarks"></a>Комментарии

Предикат типа, результатом которого является значение, **`true`** Если тип *T* может быть создан с помощью операции перемещения. Этот предикат эквивалентен `is_constructible<T, T&&>`. Тип *T* , не имеющий конструктора перемещения, но имеющий конструктор копии, принимающий `const T&` аргумент, соответствует `std::is_move_constructible` .

## <a name="requirements"></a>Требования

**Заголовок:**\<type_traits>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[<type_traits>](../standard-library/type-traits.md)
