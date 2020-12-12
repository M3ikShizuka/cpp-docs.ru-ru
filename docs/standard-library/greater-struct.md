---
description: 'Дополнительные сведения о: больше структуры'
title: Структура greater
ms.date: 11/04/2016
f1_keywords:
- functional/std::greater
helpviewer_keywords:
- greater struct
- greater function
ms.assetid: ebc348e1-edcd-466b-b21a-db95bd8f9079
ms.openlocfilehash: fabee76d20d201f63b9f5397c20409ad62125657
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97324178"
---
# <a name="greater-struct"></a>Структура greater

Бинарный предикат, который выполняет операцию "больше чем" ( `operator>` ) для своих аргументов.

## <a name="syntax"></a>Синтаксис

```cpp
template <class Type = void>
struct greater : public binary_function <Type, Type, bool>
{
    bool operator()(
    const Type& Left,
    const Type& Right) const;

};

// specialized transparent functor for operator>
template <>
struct greater<void>
{
  template <class T, class U>
  auto operator()(T&& Left, U&& Right) const
    ->  decltype(std::forward<T>(Left)> std::forward<U>(Right));
};
```

### <a name="parameters"></a>Параметры

*Тип*, *T*, *U*\
Любой тип, поддерживающий `operator>`, принимающий операнды указанного или выводимого типа.

*Слева*\
Левый операнд в операции "больше чем". Неспециализированный шаблон принимает ссылочный аргумент lvalue типа *Type*. Специализированный шаблон выполняет точную пересылку ссылочных аргументов lvalue и rvalue для выводимого типа *T*.

*Правильно*\
Правый операнд в операции "больше чем". Неспециализированный шаблон принимает ссылочный аргумент lvalue типа *Type*. Специализированный шаблон выполняет точную пересылку ссылочных аргументов lvalue и rvalue для выводимого типа *U*.

## <a name="return-value"></a>Возвращаемое значение

Результат `Left > Right`. Специализированный шаблон выполняет точную пересылку результата типа, возвращаемого `operator>`.

## <a name="remarks"></a>Комментарии

Бинарный предикат `greater` < `Type`> обеспечивает строгое слабое упорядочение набора значений элементов типа *Type* в классы эквивалентности, только если этот тип удовлетворяет стандартным математическим требованиям для такого упорядочения. Специализации для любого типа указателя дают общее упорядочение элементов в том, что все элементы из различных значений упорядочиваются относительно друг друга.

## <a name="example"></a>Пример

```cpp
// functional_greater.cpp
// compile with: /EHsc
#include <vector>
#include <algorithm>
#include <functional>
#include <cstdlib>
#include <iostream>

int main( )
{
   using namespace std;
   vector <int> v1;
   vector <int>::iterator Iter1;

   int i;
   for ( i = 0 ; i < 8 ; i++ )
   {
      v1.push_back( rand( ) );
   }

   cout << "Original vector v1 = ( " ;
   for ( Iter1 = v1.begin( ) ; Iter1 != v1.end( ) ; Iter1++ )
      cout << *Iter1 << " ";
   cout << ")" << endl;

   // To sort in ascending order,
   // use default binary predicate less<int>( )
   sort( v1.begin( ), v1.end( ) );
   cout << "Sorted vector v1 = ( " ;
   for ( Iter1 = v1.begin( ) ; Iter1 != v1.end( ) ; Iter1++ )
      cout << *Iter1 << " ";
   cout << ")" << endl;

   // To sort in descending order,
   // specify binary predicate greater<int>( )
   sort( v1.begin( ), v1.end( ), greater<int>( ) );
   cout << "Resorted vector v1 = ( " ;
   for ( Iter1 = v1.begin( ) ; Iter1 != v1.end( ) ; Iter1++ )
      cout << *Iter1 << " ";
   cout << ")" << endl;
}
```

```Output
Original vector v1 = (41 18467 6334 26500 19169 15724 11478 29358)
Sorted vector v1 = (41 6334 11478 15724 18467 19169 26500 29358)
Resorted vector v1 = (29358 26500 19169 18467 15724 11478 6334 41)
```
