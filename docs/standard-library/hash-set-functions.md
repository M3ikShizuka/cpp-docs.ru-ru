---
description: 'Дополнительные сведения: &lt; функции hash_set &gt;'
title: Функции &lt;hash_set&gt;
ms.date: 11/04/2016
f1_keywords:
- hash_set/std::swap
- hash_set/std::swap (hash_multiset)
ms.assetid: 557a0162-3728-4537-97dc-f9f6cc7ece94
ms.openlocfilehash: 7040325f3af26052306b1ebd90f1919d96dcbf19
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97231800"
---
# <a name="lthash_setgt-functions"></a>Функции &lt;hash_set&gt;

[позиции](#swap)\
[Swap (hash_multiset)](#swap_hash_multiset)

## <a name="swap"></a><a name="swap"></a> позиции

> [!NOTE]
> Этот API устарел. Вместо него следует использовать [класс unordered_set](../standard-library/unordered-set-class.md).

Выполняет обмен элементами между двумя объектами hash_set.

```cpp
void swap(
    hash_set <Key, Traits, Allocator>& left,
    hash_set <Key, Traits, Allocator>& right);
```

### <a name="parameters"></a>Параметры

*Правильно*\
Hash_set, предоставляющая элементы для переключения, или hash_set, элементы которого должны быть заменены элементами hash_set *Left*.

*слева*\
Hash_set, элементы которой должны быть заменены элементами hash_set *right*.

### <a name="remarks"></a>Комментарии

`swap`Функция-шаблон — это алгоритм, специализированный для класса контейнера hash_set для выполнения функции-члена `left.` [Swap](../standard-library/hash-set-class.md#swap)( `right` ). Это экземпляр частичного упорядочивания шаблонов функций компилятором. Когда функции-шаблоны перегружаются таким образом, что соответствие шаблона и вызова функции не является уникальным, компилятор выберет наиболее специализированную версию функции-шаблона. Общая версия функции-шаблона

**шаблон \<class T> void-swap (t&, t&),**

в классе алгоритма работает путем назначения и является медленной операцией. Специализированная версия в каждом контейнере работает гораздо быстрее, так как она может работать с внутренним представлением класса контейнера.

### <a name="example"></a>Пример

См. пример кода для функции-члена [hash_set::swap](../standard-library/hash-set-class.md#swap), в котором используется версия шаблона `swap`.

## <a name="swap-hash_multiset"></a><a name="swap_hash_multiset"></a> Swap (hash_multiset)

> [!NOTE]
> Этот API устарел. Вместо него следует использовать [класс unordered_set](../standard-library/unordered-set-class.md).

Обменивает местами элементы двух объектов hash_multiset.

```cpp
void swap(hash_multiset <Key, Traits, Allocator>& left, hash_multiset <Key, Traits, Allocator>& right);
```

### <a name="parameters"></a>Параметры

*Правильно*\
Hash_multiset, предоставляющая элементы для переключения, или hash_multiset, элементы которого должны быть заменены элементами hash_multiset *Left*.

*слева*\
Hash_multiset, элементы которой должны быть заменены элементами hash_multiset *right*.

### <a name="remarks"></a>Комментарии

`swap`Функция-шаблон — это алгоритм, специализированный для класса контейнера hash_multiset для выполнения функции-члена `left.` [Swap](../standard-library/hash-multiset-class.md#swap)( `right` ). Это экземпляр частичного упорядочивания шаблонов функций компилятором. Когда функции-шаблоны перегружаются таким образом, что соответствие шаблона и вызова функции не является уникальным, компилятор выберет наиболее специализированную версию функции-шаблона. Общая версия функции-шаблона

**шаблон \<class T> void-swap (t&, t&),**

в классе алгоритма работает путем назначения и является медленной операцией. Специализированная версия в каждом контейнере работает гораздо быстрее, так как она может работать с внутренним представлением класса контейнера.

### <a name="example"></a>Пример

См. пример кода для функции-члена [hash_multiset::swap](../standard-library/hash-multiset-class.md#swap), в котором используется версия шаблона `swap`.

## <a name="see-also"></a>См. также раздел

[<hash_set>](../standard-library/hash-set.md)
