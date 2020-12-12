---
description: 'Дополнительные сведения о: logical_not struct'
title: Структура logical_not
ms.date: 11/04/2016
f1_keywords:
- functional/std::logical_not
helpviewer_keywords:
- logical_not class
- logical_not struct
ms.assetid: 892db678-31da-4540-974b-17b05efc0849
ms.openlocfilehash: dc89a5a764d9f3182609b47c5f05eb8b3e167cec
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97277691"
---
# <a name="logical_not-struct"></a>Структура logical_not

Стандартный объект функции, выполняющий логическую операцию NOT ( `operator!` ) для своего аргумента.

## <a name="syntax"></a>Синтаксис

```
template <class Type = void>
struct logical_not : public unary_function<Type, bool>
{
    bool operator()(const Type& Left) const;
};

// specialized transparent functor for operator!
template <>
struct logical_not<void>
{
  template <class Type>
  auto operator()(Type&& Left) const`
     -> decltype(!std::forward<Type>(Left));
};
```

### <a name="parameters"></a>Параметры

*Тип*\
Любой тип, поддерживающий `operator!`, принимающий операнды указанного или выводимого типа.

*Слева*\
Операнд операции логического отрицания. Неспециализированный шаблон принимает ссылочный аргумент lvalue типа *Type*. Специализированный шаблон выполняет точную пересылку ссылочных аргументов lvalue и rvalue для выводимого *типа*.

## <a name="return-value"></a>Возвращаемое значение

Результат `!Left`. Специализированный шаблон выполняет точную пересылку результата типа, возвращаемого `operator!`.

## <a name="example"></a>Пример

```cpp
// functional_logical_not.cpp
// compile with: /EHsc
#include <deque>
#include <algorithm>
#include <functional>
#include <iostream>

int main( )
{
   using namespace std;
   deque<bool> d1, d2 ( 7 );
   deque<bool>::iterator iter1, iter2;

   int i;
   for ( i = 0 ; i < 7 ; i++ )
   {
      d1.push_back((bool)((i % 2) != 0));
   }

   cout << boolalpha;    // boolalpha I/O flag on

   cout << "Original deque:\n d1 = ( " ;
   for ( iter1 = d1.begin( ) ; iter1 != d1.end( ) ; iter1++ )
      cout << *iter1 << " ";
   cout << ")" << endl;

   // To flip all the truth values of the elements,
   // use the logical_not function object
   transform( d1.begin( ), d1.end( ), d2.begin( ),logical_not<bool>( ) );
   cout << "The deque with its values negated is:\n d2 = ( " ;
   for ( iter2 = d2.begin( ) ; iter2 != d2.end( ) ; iter2++ )
      cout << *iter2 << " ";
   cout << ")" << endl;
}
```

```Output
Original deque:
d1 = ( false true false true false true false )
The deque with its values negated is:
d2 = ( true false true false true false true )
```
