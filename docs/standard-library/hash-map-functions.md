---
description: 'Дополнительные сведения: &lt; функции hash_map &gt;'
title: Функции &lt;hash_map&gt;
ms.date: 11/04/2016
f1_keywords:
- hash_map/std::swap
- hash_map/std::swap (hash_map)
ms.assetid: 28748cd0-71f7-41b9-b068-579183645fba
ms.openlocfilehash: 50f9150bc79a3ffdc586ba420d6e3dc280784767
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97231905"
---
# <a name="lthash_mapgt-functions"></a>Функции &lt;hash_map&gt;

[позиции](#swap)\
[swap (hash_map)](#swap_hash_map)

## <a name="swap-hash_map"></a><a name="swap_hash_map"></a> Swap (hash_map)

> [!NOTE]
> Этот API устарел. Вместо него следует использовать [класс unordered_map](../standard-library/unordered-map-class.md).

Меняет местами элементы двух hash_map.

```cpp
void swap(
    hash_map <Key, Type, Traits, Alloctor>& left,
    hash_map <Key, Type, Traits, Allocator>& right);
```

### <a name="parameters"></a>Параметры

*Правильно*\
Hash_map, элементы которой должны быть заменены на те, которые расположены *слева* от схемы.

*слева*\
Hash_map, элементы которой должны быть заменены соответствующими элементами схемы *right*.

### <a name="remarks"></a>Комментарии

Функция-шаблон является специальным алгоритмом для схемы hash_map класса контейнера для выполнения функции-члена `left.`[swap](../standard-library/basic-ios-class.md#swap)*(right*). Это экземпляр частичного упорядочивания шаблонов функций компилятором. Когда функции-шаблоны перегружаются таким образом, что соответствие шаблона и вызова функции не является уникальным, компилятор выберет наиболее специализированную версию функции-шаблона. Общая версия функции шаблона, **шаблон \<class T> void swap (t&, t&)** в файле заголовка алгоритма работает по назначению и является очень высокой операцией. Специализированная версия в каждом контейнере работает гораздо быстрее, так как она может работать с внутренним представлением класса контейнера.

## <a name="swap"></a><a name="swap"></a> позиции

> [!NOTE]
> Этот API устарел. Вместо него следует использовать [unordered_multimap Class](../standard-library/unordered-multimap-class.md).

Меняет местами элементы двух hash_multimap.

```cpp
void swap(
    hash_multimap <Key, Type, Traits, Alloctor>& left,
    hash_multimap <Key, Type, Traits, Allocator>& right);
```

### <a name="parameters"></a>Параметры

*Правильно*\
Hash_multimap, элементы которой должны быть заменены на те, которые расположены *слева* от схемы.

*слева*\
Hash_multimap, элементы которой должны быть заменены соответствующими элементами схемы *right*.

### <a name="remarks"></a>Комментарии

Функция-шаблон является специальным алгоритмом для схемы hash_multimap класса контейнера для выполнения функции-члена `left.`[swap](../standard-library/hash-multimap-class.md#swap)*(right*`)`. Это экземпляр частичного упорядочивания шаблонов функций компилятором. Когда функции-шаблоны перегружаются таким образом, что соответствие шаблона и вызова функции не является уникальным, компилятор выберет наиболее специализированную версию функции-шаблона. Общая версия функции шаблона, **шаблон \<class T> void swap (t&, t&)** в файле заголовка алгоритма работает по назначению и является очень высокой операцией. Специализированная версия в каждом контейнере работает гораздо быстрее, так как она может работать с внутренним представлением класса контейнера.

## <a name="see-also"></a>См. также раздел

[<hash_map>](../standard-library/hash-map.md)
