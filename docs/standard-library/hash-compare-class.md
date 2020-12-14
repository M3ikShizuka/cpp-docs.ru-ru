---
description: 'Дополнительные сведения о: hash_compare классе'
title: Класс hash_compare
ms.date: 11/04/2016
f1_keywords:
- hash_set/stdext::hash_compare
helpviewer_keywords:
- hash_compare class
ms.assetid: d502bb59-de57-4585-beb9-00e3a998c0af
ms.openlocfilehash: 510de9901e58e130a53410b688c22324714b9962
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97231944"
---
# <a name="hash_compare-class"></a>Класс hash_compare

Шаблон класса описывает объект, который может использоваться любым ассоциативным контейнером хэша — hash_map, hash_multimap, hash_set или hash_multiset — как **объект параметра** признаков по умолчанию для упорядочивания и хэширования содержащихся в них элементов.

## <a name="syntax"></a>Синтаксис

class hash_compare { Traits comp; public: const size_t bucket_size = 4; const size_t min_buckets = 8; hash_compare(); hash_compare(Traits pred); size_t operator()(const Key& key) const; bool operator()( const Key& key1, const Key& key2) const; };

## <a name="remarks"></a>Комментарии

Каждый ассоциативный хэш-контейнер хранит объект-признаки типа `Traits` (параметр шаблона). Можно наследовать класс от специализации hash_compare, чтобы выборочно переопределить некоторые функции и объекты, или можно предоставить собственную версию этого класса, если выполняются определенные минимальные требования. В частности, для объекта, hash_comp типа `hash_compare<Key, Traits>` , для перечисленных выше контейнеров требуется следующее поведение:

- Для всех значений `key` типа `Key` вызов **hash_comp**( `key` ) служит хэш-функцией, которая возвращает распределение значений типа `size_t` . Функция, предоставленная hash_compare, возвращает `key`.

- Для любого значения `key1` типа `Key` , которое предшествует `key2` в последовательности и имеет то же значение хэша (значение, возвращаемое хэш-функцией), **hash_comp**( `key2` , `key1` ) имеет значение false. Функция должна накладывать итоговый порядок на значения типа `Key` . Функция, предоставляемая hash_compare, возвращает *comp*( `key2` , `key1` ) `,` , где *comp* — это сохраненный объект типа `Traits` , который можно указать при создании объекта hash_comp. Для типа параметра по умолчанию `Traits` `less<Key>` ключи сортировки никогда не уменьшаются в значении.

- Целочисленная константа `bucket_size` указывает среднее число элементов на "сегмент" (запись хэш-таблицы), которые контейнер должен не превысить. Это значение должно быть больше нуля. Значение, предоставленное hash_compare, равно 4.

- Целочисленная константа `min_buckets` указывает минимальное количество контейнеров, которые должны храниться в хэш-таблице. Оно должно быть степенью числа два и больше нуля. Значение, предоставленное hash_compare, равно 8.

## <a name="example"></a>Пример

Примеры объявления и использования hash_compare см. в примерах [hash_map::hash_map](../standard-library/hash-map-class.md#hash_map), [hash_multimap::hash_multimap](../standard-library/hash-multimap-class.md#hash_multimap), [hash_set::hash_set](../standard-library/hash-set-class.md#hash_set) и [hash_multiset::hash_multiset](../standard-library/hash-multiset-class.md#hash_multiset).

## <a name="requirements"></a>Требования

**Заголовок:**\<hash_map>

**Пространство имен:** stdext

## <a name="see-also"></a>См. также раздел

[Безопасность потоков в стандартной библиотеке C++](../standard-library/thread-safety-in-the-cpp-standard-library.md)\
[Справочник по стандартной библиотеке C++](../standard-library/cpp-standard-library-reference.md)
