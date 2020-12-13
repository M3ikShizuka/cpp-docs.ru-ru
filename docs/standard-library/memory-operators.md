---
description: Дополнительные сведения об &lt; &gt; операторах памяти
title: операторы &lt;memory&gt;
ms.date: 11/04/2016
f1_keywords:
- memory/std::operator!=
- memory/std::operator>
- memory/std::operator>=
- memory/std::operator<
- memory/std::operator<=
- memory/std::operator<<
- memory/std::operator==
ms.assetid: 257e3ba9-c4c2-4ae8-9b11-b156ba9c28de
ms.openlocfilehash: cbf52aa2af13a0eae241444d88e0eeabe7efe47b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97183949"
---
# <a name="ltmemorygt-operators"></a>операторы &lt;memory&gt;

## <a name="operator"></a><a name="op_neq"></a> operator! =

Проверяет неравенство между объектами.

```cpp
template <class Type, class Other>
bool operator!=(
    const allocator<Type>& left,
    const allocator<Other>& right) throw();

template <class T, class Del1, class U, class Del2>
bool operator!=(
    const unique_ptr<T, Del1>& left,
    const unique_ptr<U&, Del2>& right);

template <class Ty1, class Ty2>
bool operator!=(
    const shared_ptr<Ty1>& left,
    const shared_ptr<Ty2>& right);
```

### <a name="parameters"></a>Параметры

*слева*\
Один из объектов для проверки на неравенство.

*Правильно*\
Один из объектов для проверки на неравенство.

*Ty1*\
Тип, управляемый левым общим указателем.

*Ty2*\
Тип, управляемый правым общим указателем.

### <a name="return-value"></a>Возвращаемое значение

**`true`** значение, если объекты не равны; значение **`false`** , если объекты равны.

### <a name="remarks"></a>Комментарии

Первый оператор шаблона возвращает значение false. (Все распределители по умолчанию равны.)

Второй и третий операторы шаблона возвращают `!(left == right)`.

### <a name="example"></a>Пример

```cpp
// memory_op_me.cpp
// compile with: /EHsc
#include <memory>
#include <iostream>
#include <vector>

using namespace std;

int main( )
{
   allocator<double> Alloc;
   vector <char>:: allocator_type v1Alloc;

   if ( Alloc != v1Alloc )
      cout << "The allocator objects Alloc & v1Alloc not are equal."
           << endl;
   else
      cout << "The allocator objects Alloc & v1Alloc are equal."
           << endl;
}
```

```Output
The allocator objects Alloc & v1Alloc are equal.
```

### <a name="example"></a>Пример

```cpp
// std__memory__operator_ne.cpp
// compile with: /EHsc
#include <memory>
#include <iostream>

int main()
    {
    std::shared_ptr<int> sp0(new int(0));
    std::shared_ptr<int> sp1(new int(0));

    std::cout << "sp0 != sp0 == " << std::boolalpha
        << (sp0 != sp0) << std::endl;
    std::cout << "sp0 != sp1 == " << std::boolalpha
        << (sp0 != sp1) << std::endl;

    return (0);
    }
```

```Output
sp0 != sp0 == false
sp0 != sp1 == true
```

## <a name="operator"></a><a name="op_eq_eq"></a> Оператор = =

Проверяет равенство между объектами.

```cpp
template <class Type, class Other>
bool operator==(
    const allocator<Type>& left,
    const allocator<Other>& right) throw();

template <class Ty1, class Del1, class Ty2, class Del2>
bool operator==(
    const unique_ptr<Ty1, Del1>& left,
    const unique_ptr<Ty2, Del2>& right);

template <class Ty1, class Ty2>
bool operator==(
    const shared_ptr<Ty1>& left;,
    const shared_ptr<Ty2>& right);
```

### <a name="parameters"></a>Параметры

*слева*\
Один из объектов для проверки на равенство.

*Правильно*\
Один из объектов для проверки на равенство.

*Ty1*\
Тип, управляемый левым общим указателем.

*Ty2*\
Тип, управляемый правым общим указателем.

### <a name="return-value"></a>Возвращаемое значение

**`true`** значение, если объекты равны, **`false`** Если объекты не равны.

### <a name="remarks"></a>Комментарии

Первый оператор шаблона возвращает значение true. (Все распределители по умолчанию равны.)

Второй и третий операторы шаблона возвращают `left.get() ==  right.get()`.

### <a name="example"></a>Пример

```cpp
// memory_op_eq.cpp
// compile with: /EHsc
#include <memory>
#include <iostream>
#include <vector>

using namespace std;

int main( )
{
   allocator<char> Alloc;
   vector <int>:: allocator_type v1Alloc;

   allocator<char> cAlloc(Alloc);
   allocator<int> cv1Alloc(v1Alloc);

   if ( cv1Alloc == v1Alloc )
      cout << "The allocator objects cv1Alloc & v1Alloc are equal."
           << endl;
   else
      cout << "The allocator objects cv1Alloc & v1Alloc are not equal."
           << endl;

   if ( cAlloc == Alloc )
      cout << "The allocator objects cAlloc & Alloc are equal."
           << endl;
   else
      cout << "The allocator objects cAlloc & Alloc are not equal."
           << endl;
}
```

```Output
The allocator objects cv1Alloc & v1Alloc are equal.
The allocator objects cAlloc & Alloc are equal.
```

### <a name="example"></a>Пример

```cpp
// std__memory__operator_eq.cpp
// compile with: /EHsc
#include <memory>
#include <iostream>

int main()
    {
    std::shared_ptr<int> sp0(new int(0));
    std::shared_ptr<int> sp1(new int(0));

    std::cout << "sp0 == sp0 == " << std::boolalpha
        << (sp0 == sp0) << std::endl;
    std::cout << "sp0 == sp1 == " << std::boolalpha
        << (sp0 == sp1) << std::endl;

    return (0);
    }
```

```Output
sp0 == sp0 == true
sp0 == sp1 == false
```

## <a name="operatorgt"></a><a name="op_gt_eq"></a> станции&gt;=

Проверяет, больше или равен один объект второму объекту.

```cpp
template <class T, class Del1, class U, class Del2>
bool operator>=(
    const unique_ptr<T, Del1>& left,
    const unique_ptr<U, Del2>& right);

template <class Ty1, class Ty2>
bool operator>=(
    const shared_ptr<Ty1>& left,
    const shared_ptr<Ty2>& right);
```

### <a name="parameters"></a>Параметры

*слева*\
Один из сравниваемых объектов.

*Правильно*\
Один из сравниваемых объектов.

*Ty1*\
Тип, управляемый левым общим указателем.

*Ty2*\
Тип, управляемый правым общим указателем.

### <a name="remarks"></a>Комментарии

Операторы шаблона возвращают `left.get() >= right.get()`.

## <a name="operatorlt"></a><a name="op_lt"></a> станции&lt;

Проверяет, меньше ли один объект второго объекта.

```cpp
template <class T, class Del1, class U, class Del2>
bool operator<(
    const unique_ptr<T, Del1>& left,
    const unique_ptr<U&, Del2>& right);

template <class Ty1, class Ty2>
bool operator<(
    const shared_ptr<Ty1>& left,
    const shared_ptr<Ty2>& right);
```

### <a name="parameters"></a>Параметры

*слева*\
Один из сравниваемых объектов.

*Правильно*\
Один из сравниваемых объектов.

*Ty1*\
Тип, управляемый левым указателем.

*Ty2*\
Тип, управляемый правым указателем.

## <a name="operatorlt"></a><a name="op_lt_eq"></a> станции&lt;=

Проверяет, меньше или равен один объект второму объекту.

```cpp
template <class T, class Del1, class U, class Del2>
bool operator<=(
    const unique_ptr<T, Del1>& left,
    const unique_ptr<U&, Del2>& right);

template <class Ty1, class Ty2>
bool operator<=(
    const shared_ptr<Ty1>& left,
    const shared_ptr<Ty2>& right);
```

### <a name="parameters"></a>Параметры

*слева*\
Один из сравниваемых объектов.

*Правильно*\
Один из сравниваемых объектов.

*Ty1*\
Тип, управляемый левым общим указателем.

*Ty2*\
Тип, управляемый правым общим указателем.

### <a name="remarks"></a>Комментарии

Операторы шаблона возвращают `left.get() <= right.get()`

## <a name="operatorgt"></a><a name="op_gt"></a> станции&gt;

Проверяет, больше ли один объект второго объекта.

```cpp
template <class Ty1, class Del1, class Ty2, class Del2>
bool operator>(
    const unique_ptr<Ty1, Del1>& left,
    const unique_ptr<Ty2&, Del2gt;& right);

template <class Ty1, class Ty2>
bool operator>(
    const shared_ptr<Ty1>& left,
    const shared_ptr<Ty2>& right);
```

### <a name="parameters"></a>Параметры

*слева*\
Один из сравниваемых объектов.

*Правильно*\
Один из сравниваемых объектов.

*Ty1*\
Тип, управляемый левым общим указателем.

*Ty2*\
Тип, управляемый правым общим указателем.

## <a name="operatorltlt"></a><a name="op_lt_lt"></a> станции&lt;&lt;

Записывает в поток общий указатель.

```cpp
template <class Elem, class Tr, class Ty>
std::basic_ostream<Elem, Tr>& operator<<(std::basic_ostream<Elem, Tr>& out,
    shared_ptr<Ty>& sp);
```

### <a name="parameters"></a>Параметры

*Elem*\
Тип элемента потока.

*ТС*\
Тип признаков элемента потока.

*Ty*\
Тип, управляемый общим указателем.

*заполняет*\
Выходной поток.

*портов*\
Общий указатель.

### <a name="remarks"></a>Комментарии

Функция шаблона возвращает `out << sp.get()`.

### <a name="example"></a>Пример

```cpp
// std__memory__operator_sl.cpp
// compile with: /EHsc
#include <memory>
#include <iostream>

int main()
    {
    std::shared_ptr<int> sp0(new int(5));

    std::cout << "sp0 == " << sp0 << " (varies)" << std::endl;

    return (0);
    }
```

```Output
sp0 == 3f3040 (varies)
```
