---
description: 'Дополнительные сведения: &lt; операторы forward_list &gt;'
title: Операторы &lt;forward_list&gt;
ms.date: 11/04/2016
f1_keywords:
- forward_list/std::operator!=
- forward_list/std::operator==
- forward_list/std::operatoroperator&gt;
- forward_list/std::operatoroperator&gt=;
- forward_list/std::operatoroperator&lt;
- forward_list/std::operatoroperator&lt;=
ms.assetid: 57492e09-3836-4dbc-9ae5-78ecf506c190
helpviewer_keywords:
- std::operator!= (forward_list)
- std::operator== (forward_list)
- std::operatoroperator&gt; (forward_list)
- std::operatoroperator&gt=; (forward_list)
- std::operatoroperator&lt; (forward_list)
- std::operatoroperator&lt;= (forward_list)
ms.openlocfilehash: 39d3383e0489a544f65f18af3ff3c2b6d8f2e45d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97232360"
---
# <a name="ltforward_listgt-operators"></a>Операторы &lt;forward_list&gt;

## <a name="operator"></a><a name="op_eq_eq"></a> Оператор = =

Проверяет, равен ли объект прямого списка слева от оператора объекту прямого списка справа от оператора.

```cpp
bool operator==(
    const forward_list <Type, Allocator>& left,
    const forward_list <Type, Allocator>& right);
```

### <a name="parameters"></a>Параметры

*слева*\
Объект типа `forward_list`.

*Правильно*\
Объект типа `forward_list`.

### <a name="remarks"></a>Комментарии

Эта функция шаблона перегружается `operator==` для сравнения двух объектов шаблона класса `forward_list` . Функция возвращает `distance(left.begin(), end()) == distance(right.begin(),right.end()) && equal(left. begin(),left. end(),right.begin())`.

## <a name="operator"></a><a name="op_neq"></a> operator! =

Проверяет, не равен ли объект прямого списка слева от оператора объекту прямого списка справа от оператора.

```cpp
bool operator!=(
    const forward_list <Type, Allocator>& left,
    const forward_list <Type, Allocator>& right);
```

### <a name="parameters"></a>Параметры

*слева*\
Объект типа `forward_list`.

*Правильно*\
Объект типа `forward_list`.

### <a name="return-value"></a>Возвращаемое значение

**`true`** значение, если списки не равны; **`false`** значение, если списки равны.

### <a name="remarks"></a>Комментарии

Эта функция шаблона возвращает `!(left == right)`.

## <a name="operatorlt"></a><a name="op_lt"></a> станции&lt;

Проверяет, меньше ли объект прямого списка слева от оператора объекта прямого списка справа от оператора.

```cpp
bool operator<(
    const forward_list <Type, Allocator>& left,
    const forward_list <Type, Allocator>& right);
```

### <a name="parameters"></a>Параметры

*слева*\
Объект типа `forward_list`.

*Правильно*\
Объект типа `forward_list`.

### <a name="return-value"></a>Возвращаемое значение

**`true`** значение, если список слева от оператора меньше, но не равен списку с правой стороны оператора; в противном случае — значение **`false`** .

### <a name="remarks"></a>Комментарии

Эта функция шаблона перегружается `operator<` для сравнения двух объектов шаблона класса `forward_list` . Функция возвращает `lexicographical_compare(lhs. begin(), lhs. end(), rhs.begin(), rhs.end())`.

## <a name="operatorlt"></a><a name="op_lt_eq"></a> станции&lt;=

Проверяет, меньше ли (или равен) объект прямого списка слева от оператора объекта прямого списка справа от оператора.

```cpp
bool operator<=(
    const forward_list <Type, Allocator>& left,
    const forward_list <Type, Allocator>& right);
```

### <a name="parameters"></a>Параметры

*слева*\
Объект типа `forward_list`.

*Правильно*\
Объект типа `forward_list`.

### <a name="return-value"></a>Возвращаемое значение

**`true`** значение, если список слева от оператора меньше или равен списку с правой стороны оператора; в противном случае — значение **`false`** .

### <a name="remarks"></a>Комментарии

Эта функция шаблона возвращает `!(right < left)`.

## <a name="operatorgt"></a><a name="op_gt"></a> станции&gt;

Проверяет, больше ли объект прямого списка слева от оператора объекта прямого списка справа от оператора.

```cpp
bool operator>(
    const forward_list <Type, Allocator>& left,
    const forward_list <Type, Allocator>& right);
```

### <a name="parameters"></a>Параметры

*слева*\
Объект типа `forward_list`.

*Правильно*\
Объект типа `forward_list`.

### <a name="return-value"></a>Возвращаемое значение

**`true`** значение, если список в левой части оператора больше списка с правой стороны оператора; в противном случае — значение **`false`** .

### <a name="remarks"></a>Комментарии

Эта функция шаблона возвращает `right < left`.

## <a name="operatorgt"></a><a name="op_gt_eq"></a> станции&gt;=

Проверяет, больше ли (или равен) объект прямого списка слева от оператора объекта прямого списка справа от оператора.

```cpp
bool operator>=(
    const forward_list <Type, Allocator>& left,
    const forward_list <Type, Allocator>& right);
```

### <a name="parameters"></a>Параметры

*слева*\
Объект типа `forward_list`.

*Правильно*\
Объект типа `forward_list`.

### <a name="return-value"></a>Возвращаемое значение

**`true`** значение, если прямой список в левой части оператора больше или равен прямому списку справа от оператора; в противном случае — значение **`false`** .

### <a name="remarks"></a>Комментарии

Функция шаблона возвращает `!(left < right)`.
