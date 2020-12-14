---
description: 'Дополнительные сведения: &lt; операторы типа Variant &gt;'
title: '&lt;операторы типа Variant &gt;'
ms.date: 04/04/2019
f1_keywords:
- variant/std::operator!=
- variant/std::operator==
- variant/std::operatoroperator&gt;
- variant/std::operatoroperator&gt=;
- variant/std::operatoroperator&lt;
- variant/std::operatoroperator&lt;=
helpviewer_keywords:
- std::operator!= (variant)
- std::operator== (variant)
- std::operatoroperator&gt; (variant)
- std::operatoroperator&gt=; (variant)
- std::operatoroperator&lt; (variant)
- std::operatoroperator&lt;= (variant)
ms.openlocfilehash: 3315c73ea529ad7ade4f32be3784a43bda07ac26
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97312830"
---
# <a name="ltvariantgt-operators"></a>&lt;операторы типа Variant &gt;

## <a name="operator"></a><a name="op_eq_eq"></a> Оператор = =

Проверяет, равен ли объект прямого списка слева от оператора объекту прямого списка справа от оператора.

```cpp
template <class... Types>
    constexpr bool operator==(const variant<Types...>&, const variant<Types...>&);
```

## <a name="operator"></a><a name="op_neq"></a> operator! =

Проверяет, не равен ли объект прямого списка слева от оператора объекту прямого списка справа от оператора.

```cpp
template <class... Types>
    constexpr bool operator!=(const variant<Types...>&, const variant<Types...>&);
```

## <a name="operatorlt"></a><a name="op_lt"></a> станции&lt;

Проверяет, меньше ли объект прямого списка слева от оператора объекта прямого списка справа от оператора.

```cpp
template <class... Types>
    constexpr bool operator<(const variant<Types...>&, const variant<Types...>&);
```

## <a name="operatorlt"></a><a name="op_lt_eq"></a> станции&lt;=

Проверяет, меньше ли (или равен) объект прямого списка слева от оператора объекта прямого списка справа от оператора.

```cpp
template <class... Types>
    constexpr bool operator<=(const variant<Types...>&, const variant<Types...>&);
```

## <a name="operatorgt"></a><a name="op_gt"></a> станции&gt;

Проверяет, больше ли объект прямого списка слева от оператора объекта прямого списка справа от оператора.

```cpp
template <class... Types> constexpr
    bool operator>(const variant<Types...>&, const variant<Types...>&);
```

## <a name="operatorgt"></a><a name="op_gt_eq"></a> станции&gt;=

Проверяет, больше ли (или равен) объект прямого списка слева от оператора объекта прямого списка справа от оператора.

```cpp
template <class... Types> constexpr
    bool operator>=(const variant<Types...>&, const variant<Types...>&);
```
