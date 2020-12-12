---
description: 'Дополнительные сведения о: tuple_size классе;'
title: Класс tuple_size
ms.date: 11/04/2016
f1_keywords:
- tuple_size
- std::tuple_size
- utility/std::tuple_size
helpviewer_keywords:
- std::tuple_size
ms.assetid: 73852fc5-eb68-41f1-8379-465cedc2314a
ms.openlocfilehash: e825acc02e27a8d0c1ae29e5bfcf4ac1e0a708b8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97168882"
---
# <a name="tuple_size-class"></a>Класс tuple_size

Передает число элементов, содержащихся в кортеже `tuple` .

## <a name="syntax"></a>Синтаксис

```cpp
// TEMPLATE STRUCT tuple_size
template <class Tuple>
   struct tuple_size;

// number of elements in array
template <class Elem, size_t Size>
   struct tuple_size<array<Elem, Size>>
      : integral_constant<size_t, Size>;

// size of pair
template <class T1, class T2>
   struct tuple_size<pair<T1, T2>>
      : integral_constant<size_t, 2>

// size of tuple
template <class... Types>
   struct tuple_size<tuple<Types...>>
      : integral_constant<size_t, sizeof...(Types)>;

// size of const tuple
template <class Tuple>
   struct tuple_size<const Tuple>;

// size of volatile tuple
template <class Tuple>
   struct tuple_size<volatile Tuple>;

// size of const volatile tuple
template <class Tuple>
   struct tuple_size<const volatile Tuple>;
```

```cpp
template <class T> inline constexpr size_t tuple_size_v = tuple_size<T>::value;
```

### <a name="parameters"></a>Параметры

*Кортеж*\
Тип кортежа.

*Elem*\
Тип элементов массива.

*Изменять*\
Размер массива.

*T1*\
Тип первого элемента пары.

*T2*\
Тип второго элемента пары.

*Типов*\
Типы элементов кортежа.

## <a name="remarks"></a>Комментарии

Шаблон класса содержит элемент `value` , являющийся целочисленным константным выражением, значение которого является экстентом *кортежа* типа кортежа.

Специализация шаблона для массивов имеет элемент `value` , являющийся целочисленным константным выражением, значение *size* которого равно размеру массива.

В специализации шаблона для пар есть член `value`, который представляет собой интегральное константное выражение со значением 2.

## <a name="example"></a>Пример

```cpp
#include <tuple>
#include <iostream>

using namespace std;

typedef tuple<int, double, int, double> MyTuple;
int main()
{
    MyTuple c0(0, 1.5, 2, 3.7);

    // display contents "0 1 2 3"
    cout << get<0>(c0);
    cout << " " << get<1>(c0);
    cout << " " << get<2>(c0);
    cout << " " << get<3>(c0) << endl;

    // display size "4"
    cout << " " << tuple_size<MyTuple>::value << endl;
}
```

```Output
0 1.5 2 3.7
4
```

## <a name="requirements"></a>Требования

**Заголовок:**\<tuple>

**Заголовок:** \<array> (для специализации массива)

**Заголовок:** \<utility> (для специализации пары)

**Пространство имен:** std
