---
description: 'Дополнительные сведения о: iterator_traits struct'
title: Структура iterator_traits
ms.date: 11/04/2016
f1_keywords:
- xutility/std::iterator_traits
helpviewer_keywords:
- iterator_traits struct
- iterator_traits class
ms.assetid: 8b92c2c5-f658-402f-8ca1-e7ae301b8514
ms.openlocfilehash: ac97b84ff7bcedc00f2b069ce05f734ac65618ee
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97289687"
---
# <a name="iterator_traits-struct"></a>Структура iterator_traits

Вспомогательная структура-шаблон, используется для указания всех критических определений типов, которые должен иметь итератор.

## <a name="syntax"></a>Синтаксис

```cpp
struct iterator_traits {
   typedef typename Iterator::iterator_category iterator_category;
   typedef typename Iterator::value_type value_type;
   typedef typename Iterator::difference_type difference_type;
   typedef difference_type distance_type;
   typedef typename Iterator::pointer pointer;
   typedef typename Iterator::reference reference;
   };
```

## <a name="remarks"></a>Remarks

Структура-шаблон определяет типы элементов

- `iterator_category`: синоним для `Iterator::iterator_category` .

- `value_type`: синоним для `Iterator::value_type` .

- `difference_type`: синоним для `Iterator::difference_type` .

- `distance_type`: синоним для `Iterator::difference_type.`

- `pointer`: синоним для `Iterator::pointer` .

- `reference`: синоним для `Iterator::reference` .

Частичные специализации определяют критические типы, связанные с указателем на объект **типа** <strong>\*</strong> или типа **const** <strong>\*</strong> .

В этой реализации вы также можете применить несколько шаблонов функций, которые не используют частичную специализацию:

```cpp
template <class Category, class Type, class Diff>
C _Iter_cat(const iterator<Category, Ty, Diff>&);

template <class Ty>
random_access_iterator_tag _Iter_cat(const Ty *);

template <class Category, class Ty, class Diff>
Ty *val_type(const iterator<Category, Ty, Diff>&);

template <class Ty>
Ty *val_type(const Ty *);

template <class Category, class Ty, class Diff>
Diff *_Dist_type(const iterator<Category, Ty, Diff>&);

template <class Ty>
ptrdiff_t *_Dist_type(const Ty *);
```

что определяет некоторые из тех же типов более косвенно. Используйте эти функции как аргументы для вызова функции. Их единственная цель — предоставить полезный параметр шаблона класса вызываемой функции.

## <a name="example"></a>Пример

```cpp
// iterator_traits.cpp
// compile with: /EHsc
#include <iostream>
#include <iterator>
#include <vector>
#include <list>

using namespace std;

template< class it >
void
function( it i1, it i2 )
{
   iterator_traits<it>::iterator_category cat;
   cout << typeid( cat ).name( ) << endl;
   while ( i1 != i2 )
   {
      iterator_traits<it>::value_type x;
      x = *i1;
      cout << x << " ";
      i1++;
   };
   cout << endl;
};

int main( )
{
   vector<char> vc( 10,'a' );
   list<int> li( 10 );
   function( vc.begin( ), vc.end( ) );
   function( li.begin( ), li.end( ) );
}
/* Output:
struct std::random_access_iterator_tag
a a a a a a a a a a
struct std::bidirectional_iterator_tag
0 0 0 0 0 0 0 0 0 0
*/
```

## <a name="requirements"></a>Требования

**Заголовок:**\<iterator>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[\<iterator>](../standard-library/iterator.md)\
[Безопасность потоков в стандартной библиотеке C++](../standard-library/thread-safety-in-the-cpp-standard-library.md)\
[Справочник по стандартной библиотеке C++](../standard-library/cpp-standard-library-reference.md)
