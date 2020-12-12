---
description: 'Дополнительные сведения: &lt; функции unordered_set &gt;'
title: Функции &lt;unordered_set&gt;
ms.date: 11/04/2016
f1_keywords:
- unordered_set/std::swap (set)
- unordered_set/std::swap (unordered_multiset)
ms.assetid: 66b35671-4023-4411-ad50-83786580d8ee
ms.openlocfilehash: 852536a5c5bdfe5d944f3b70581a313a56dc8742
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97153763"
---
# <a name="ltunordered_setgt-functions"></a>Функции &lt;unordered_set&gt;

## <a name="swap-unordered_set"></a><a name="swap"></a> Swap (unordered_set)

Меняет местами содержимое двух контейнеров.

```cpp
template <class Key, class Hash, class Pred, class Alloc>
void swap(
   unordered_set <Key, Hash, Pred, Alloc>& left,
   unordered_set <Key, Hash, Pred, Alloc>& right);
```

### <a name="parameters"></a>Параметры

*Раздел*\
Тип ключа.

*Функции*\
Тип объекта хэш-функции.

*Возможен*\
Тип объекта функции сравнения на предмет равенства.

*Идентификатор*\
Класс распределителя.

*слева*\
Первый контейнер для замены.

*Правильно*\
Второй контейнер для замены.

### <a name="remarks"></a>Комментарии

Функция шаблона выполняет `left.` [unordered_set:: Swap](../standard-library/unordered-set-class.md#swap) `(right)` .

### <a name="example"></a>Пример

```cpp
#include <unordered_set>
#include <iostream>

typedef std::unordered_set<char> Myset;
int main()
{
Myset c1;

c1.insert('a');
c1.insert('b');
c1.insert('c');

// display contents " [c] [b] [a]"
for (Myset::const_iterator it = c1.begin();
it != c1.end(); ++it)
std::cout << " [" << *it << "]";
std::cout << std::endl;

Myset c2;

c2.insert('d');
c2.insert('e');
c2.insert('f');

c1.swap(c2);

// display contents " [f] [e] [d]"
for (Myset::const_iterator it = c1.begin();
it != c1.end(); ++it)
std::cout << " [" << *it << "]";
std::cout << std::endl;

swap(c1, c2);

// display contents " [c] [b] [a]"
for (Myset::const_iterator it = c1.begin();
it != c1.end(); ++it)
std::cout << " [" << *it << "]";
std::cout << std::endl;

return (0);
}
```

```Output
[c] [b] [a]
[f] [e] [d]
[c] [b] [a]
```

## <a name="swap-unordered_multiset"></a><a name="swap_unordered_multiset"></a> Swap (unordered_multiset)

Меняет местами содержимое двух контейнеров.

```cpp
template <class Key, class Hash, class Pred, class Alloc>
void swap(
   unordered_multiset <Key, Hash, Pred, Alloc>& left,
   unordered_multiset <Key, Hash, Pred, Alloc>& right);
```

### <a name="parameters"></a>Параметры

*Раздел*\
Тип ключа.

*Функции*\
Тип объекта хэш-функции.

*Возможен*\
Тип объекта функции сравнения на предмет равенства.

*Идентификатор*\
Класс распределителя.

*слева*\
Первый контейнер для замены.

*Правильно*\
Второй контейнер для замены.

### <a name="remarks"></a>Комментарии

Функция шаблона выполняет `left.` [unordered_multiset:: Swap](../standard-library/unordered-multiset-class.md#swap) `(right)` .

### <a name="example"></a>Пример

```cpp
// std__unordered_set__u_ms_swap.cpp
// compile with: /EHsc
#include <unordered_set>
#include <iostream>

typedef std::unordered_multiset<char> Myset;
int main()
{
    Myset c1;

    c1.insert('a');
    c1.insert('b');
    c1.insert('c');

    // display contents " [c] [b] [a]"
    for (Myset::const_iterator it = c1.begin();
        it != c1.end(); ++it)
        std::cout << " [" << *it << "]";
    std::cout << std::endl;

    Myset c2;

    c2.insert('d');
    c2.insert('e');
    c2.insert('f');

    c1.swap(c2);

    // display contents " [f] [e] [d]"
    for (Myset::const_iterator it = c1.begin();
        it != c1.end(); ++it)
        std::cout << " [" << *it << "]";
    std::cout << std::endl;

    swap(c1, c2);

    // display contents " [c] [b] [a]"
    for (Myset::const_iterator it = c1.begin();
        it != c1.end(); ++it)
        std::cout << " [" << *it << "]";
    std::cout << std::endl;

    return (0);
}
```

```Output
[c] [b] [a]
[f] [e] [d]
[c] [b] [a]
```
