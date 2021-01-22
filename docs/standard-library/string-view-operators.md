---
title: '&lt;&gt;операторы string_view'
description: Справочник по API для `string_view` операторов, которые используются для сравнения двух `string_view` объектов, `string_view` а также и другого строкового объекта
ms.date: 01/15/2021
f1_keywords:
- xstring/basic_string_view::operator!=
- xstring/basic_string_view::operator&gt;
- xstring/basic_string_view::operator&gt;=
- xstring/basic_string_view::operator&lt;
- xstring/basic_string_view::operator&lt;&lt;
- xstring/basic_string_view::operator&lt;=
- xstring/basic_string_view::operator+
- xstring/basic_string_view::operator==
- xstring/std::literals::string_view_literals::operator "sv
- std::literals::string_view_literals::operator sv
- std::literals::string_view_literals
- string_view_literals
helpviewer_keywords:
- std::basic_string_view::operator!=
- std::basic_string_view::operator&gt;
- std::basic_string_view::operator&gt;=
- std::basic_string_view::operator&lt;
- std::basic_string_view::operator&lt;&lt;
- std::basic_string_view::operator&lt;=, std::basic_string_view::operator==
ms.openlocfilehash: a14d82dc0b29f88cb25f5b24f0836f033d2b828e
ms.sourcegitcommit: 3d9cfde85df33002e3b3d7f3509ff6a8dc4c0a21
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/21/2021
ms.locfileid: "98666905"
---
# <a name="string_view-operators"></a>Операторы `<string_view>`

Эти операторы используются для сравнения двух `string_view` объектов, а также `string_view` и другого строкового объекта (например [`std::string`](basic-string-class.md) , или `char*` ), для которого предоставляется неявное преобразование.

[`operator!=`](#op_neq)\
[`operator>`](#op_gt)\
[`operator>=`](#op_gt_eq)\
[`operator<`](#op_lt)\
[`operator<<`](#op_lt_lt)\
[`operator<=`](#op_lt_eq)\
[`operator==`](#op_eq_eq)\
[`operator""sv`](#op_sv)

## <a name="operator"></a><a name="op_neq"></a> `operator!=`

Проверяет неравенство объекта слева от оператора объекту справа от оператора.

```cpp
template <class CharType, class Traits>
bool operator!=(
    const basic_string_view<CharType, Traits>& left,
    const basic_string_view<CharType, Traits>& right);

template <class CharType, class Traits>
bool operator!=(
    const basic_string_view<CharType, Traits>& left,
    convertible_string_type right);

template <class CharType, class Traits>
bool operator!=(
    convertible_string_type left,
    const basic_string_view<CharType, Traits>& right);
```

### <a name="parameters"></a>Параметры

*слева*\
Любой преобразуемый строковый тип или объект `basic_string_view` сравниваемого типа.

*Правильно*\
Любой преобразуемый строковый тип или объект `basic_string_view` сравниваемого типа.

### <a name="return-value"></a>Возвращаемое значение

**`true`** Если объект в левой части оператора не лексикографически равным объекту с правой стороны; в противном случае — значение **`false`** .

### <a name="remarks"></a>Примечания

Неявное преобразование должно существовать из *convertible_string_type* на `string_view` другую сторону.

Сравнение основано на парном лексикографическом сравнении последовательностей символов. Если число элементов равно количеству и все элементы равны, то два объекта равны. В противном случае они не равны.

## <a name="operator"></a><a name="op_eq_eq"></a> `operator==`

Проверяет равенство объекта слева от оператора объекту справа от оператора.

```cpp
template <class CharType, class Traits>
bool operator==(
    const basic_string_view<CharType, Traits>& left,
    const basic_string_view<CharType, Traits>& right);

template <class CharType, class Traits>
bool operator==(
    const basic_string_view<CharType, Traits>& left,
    convertible_string_type right);

template <class CharType, class Traits>
bool operator==(
    convertible_string_type left,
    const basic_string_view<CharType, Traits>& right);
```

### <a name="parameters"></a>Параметры

*слева*\
Любой преобразуемый строковый тип или объект `basic_string_view` сравниваемого типа.

*Правильно*\
Любой преобразуемый строковый тип или объект `basic_string_view` сравниваемого типа.

### <a name="return-value"></a>Возвращаемое значение

**`true`** значение, если объект слева от оператора лексикографически равен объекту в правой части; в противном случае — значение **`false`** .

### <a name="remarks"></a>Примечания

Неявное преобразование должно существовать из *convertible_string_type* на `string_view` другую сторону.

Сравнение основано на парном лексикографическом сравнении последовательностей символов. Если число элементов равно количеству и все элементы равны, то два объекта равны.

## <a name="operator"></a><a name="op_lt"></a> `operator<`

Проверяет, что объект слева от оператора меньше, чем объект справа от оператора.

```cpp
template <class CharType, class Traits>
bool operator<(
    const basic_string_view<CharType, Traits>& left,
    const basic_string_view<CharType, Traits>& right);

template <class CharType, class Traits>
bool operator<(
    const basic_string_view<CharType, Traits>& left,
    convertible_string_type right);

template <class CharType, class Traits>
bool operator<(
    convertible_string_type left,
    const basic_string_view<CharType, Traits>& right);
```

### <a name="parameters"></a>Параметры

*слева*\
Любой преобразуемый строковый тип или объект `basic_string_view` сравниваемого типа.

*Правильно*\
Любой преобразуемый строковый тип или объект `basic_string_view` сравниваемого типа.

### <a name="return-value"></a>Возвращаемое значение

**`true`** значение, если объект слева от оператора лексикографически меньше объекта с правой стороны; в противном случае — значение **`false`** .

### <a name="remarks"></a>Примечания

Неявное преобразование должно существовать из *convertible_string_type* string_view на другой стороне.

Сравнение основано на парном лексикографическом сравнении последовательностей символов. При обнаружении первой неравной пары символов возвращается результат этого сравнения. Если неравные символы не найдены, но одна последовательность короче, более короткая последовательность меньше чем длинная. Иными словами, "Cat" меньше "кошки".

### <a name="example"></a>Пример

```cpp
#include <string>
#include <string_view>

using namespace std;

int main()
{
    string_view sv1 { "ABA" };
    string_view sv2{ "ABAC" };
    string_view sv3{ "ABAD" };
    string_view sv4{ "ABACE" };

    bool result = sv2 > sv1; // true
    result = sv3 > sv2; // true
    result = sv3 != sv1; // true
    result = sv4 < sv3; // true because `C` < `D`
}
```

## <a name="operator"></a><a name="op_lt_eq"></a> `operator<=`

Проверяет, что объект слева от оператора меньше или равен объекту справа от оператора.

```cpp
template <class CharType, class Traits>
bool operator<=(
    const basic_string_view<CharType, Traits>& left,
    const basic_string_view<CharType, Traits>& right);

template <class CharType, class Traits>
bool operator<=(
    const basic_string_view<CharType, Traits>& left,
    convertible_string_type right);

template <class CharType, class Traits>
bool operator<=(
    convertible_string_type left,
    const basic_string_view<CharType, Traits>& right);
```

### <a name="parameters"></a>Параметры

*слева*\
Любой преобразуемый строковый тип или объект `basic_string_view` сравниваемого типа.

*Правильно*\
Любой преобразуемый строковый тип или объект `basic_string_view` сравниваемого типа.

### <a name="return-value"></a>Возвращаемое значение

**`true`** значение, если объект слева от оператора лексикографически меньше или равен объекту в правой части; в противном случае — значение **`false`** .

### <a name="remarks"></a>Примечания

См. раздел [`operator<`](#op_lt).

## <a name="operator"></a><a name="op_lt_lt"></a> `operator<<`

Записывает в `string_view` выходной поток.

```cpp
template <class CharType, class Traits>
inline basic_ostream<CharType, Traits>& operator<<(
    basic_ostream<CharType, Traits>& Ostr, const basic_string_view<CharType, Traits> Str);
```

### <a name="parameters"></a>Параметры

*`Ostr`*\
поток вывода, в который выполняется запись.

*`Str`*\
String_view, который необходимо указать в потоке вывода.

### <a name="return-value"></a>Возвращаемое значение

поток вывода, в который выполняется запись.

### <a name="remarks"></a>Примечания

Этот оператор используется для вставки содержимого в `string_view` поток вывода, например с помощью [`std::cout`](iostream.md#cout) .

## <a name="operator"></a><a name="op_gt"></a> `operator>`

Проверяет, что объект слева от оператора больше, чем объект справа от оператора.

```cpp
template <class CharType, class Traits>
bool operator>(
    const basic_string_view<CharType, Traits>& left,
    const basic_string_view<CharType, Traits>& right);

template <class CharType, class Traits>
bool operator>(
    const basic_string_view<CharType, Traits>& left,
    convertible_string_type right);

template <class CharType, class Traits>
bool operator>(
    convertible_string_type left,
    const basic_string_view<CharType, Traits>& right);
```

### <a name="parameters"></a>Параметры

*слева*\
Любой преобразуемый строковый тип или объект `basic_string_view` сравниваемого типа.

*Правильно*\
Любой преобразуемый строковый тип или объект `basic_string_view` сравниваемого типа.

### <a name="return-value"></a>Возвращаемое значение

**`true`** значение, если объект в левой части оператора лексикографически больше `string_view` объекта с правой стороны; в противном случае — **`false`** .

### <a name="remarks"></a>Примечания

См. раздел [`operator<`](#op_lt).

## <a name="operator"></a><a name="op_gt_eq"></a> `operator>=`

Проверяет, что объект слева от оператора больше или равен объекту справа от оператора.

```cpp
template <class CharType, class Traits>
bool operator>=(
    const basic_string_view<CharType, Traits>& left,
    const basic_string_view<CharType, Traits>& right);

template <class CharType, class Traits>
bool operator>=(
    const basic_string_view<CharType, Traits>& left,
    convertible_string_type right);

template <class CharType, class Traits>
bool operator>=(
    convertible_string_type left,
    const basic_string_view<CharType, Traits>& right);
```

### <a name="parameters"></a>Параметры

*`left`*\
Любой преобразуемый строковый тип или объект `basic_string_view` сравниваемого типа.

*`right`*\
Любой преобразуемый строковый тип или объект `basic_string_view` сравниваемого типа.

### <a name="return-value"></a>Возвращаемое значение

**`true`** значение, если объект слева от оператора лексикографически больше или равен объекту с правой стороны; в противном случае — значение **`false`** .

### <a name="remarks"></a>Примечания

См. раздел [`operator<`](#op_lt).

## <a name="operator-sv-string_view-literal"></a><a name="op_sv"></a>`operator"" sv`( `string_view` литерал)

Конструирует объект `string_view` из строкового литерала. Требуется пространство имен `std::literals::string_view_literals` .

### <a name="example"></a>Пример

```cpp

using namespace std;
using namespace literals::string_view_literals;

    string_view sv{ "Hello"sv };
    wstring_view wsv{ L"Hello"sv };
    u16string_view sv16{ u"Hello"sv };
    u32string_view sv32{ U"Hello"sv };
```

## <a name="requirements"></a>Требования

[`/std:c++17`](../build/reference/std-specify-language-standard-version.md)

## <a name="see-also"></a>См. также раздел

[`<string_view>`](../standard-library/string-view.md)
