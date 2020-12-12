---
description: 'Дополнительные сведения о: is_literal_type классе'
title: Класс is_literal_type
ms.date: 11/04/2016
f1_keywords:
- type_traits/std::is_literal_type
helpviewer_keywords:
- is_literal_type
ms.assetid: a03a4ebb-ee66-48d6-91bb-41cf72b2401f
ms.openlocfilehash: 97cb609c5a42bed0be205b1b51ff901d3e366bb1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97323690"
---
# <a name="is_literal_type-class"></a>Класс is_literal_type

Проверяет, может ли тип использоваться в качестве **`constexpr`** переменной или быть создан, использован или возвращен из **`constexpr`** функций.

## <a name="syntax"></a>Синтаксис

```cpp
template <class T>
struct is_literal_type;
```

### <a name="parameters"></a>Параметры

*T*\
Запрашиваемый тип.

## <a name="remarks"></a>Комментарии

Экземпляр предиката типа содержит значение true, если тип *T* является *типом литерала*, в противном случае — значение false. Литеральный тип является либо **`void`** скалярным типом, ссылочным типом, массивом типа литерала, либо типом класса литерала. Тип класса литерала — это тип класса, который имеет тривиальный деструктор, является либо агрегатным типом, либо имеет по крайней мере один конструктор без перемещения, не являющийся копией **`constexpr`** , а все его базовые классы и нестатические элементы данных являются типами литералов, не являющимися переменными. Хотя тип литерала всегда является литералом, понятие типа литерала включает все, что компилятор может вычислить как **`constexpr`** во время компиляции.

## <a name="requirements"></a>Требования

**Заголовок:**\<type_traits>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[<type_traits>](../standard-library/type-traits.md)
