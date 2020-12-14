---
description: 'Дополнительные сведения: &lt; hash_set&gt;'
title: '&lt;hash_set&gt;'
ms.date: 11/04/2016
f1_keywords:
- <hash_set>
- std::<hash_set>
helpviewer_keywords:
- hash_set header
ms.assetid: 6b556967-c808-4869-9b4d-f9e030864435
ms.openlocfilehash: 353ec0a4f57662380e912893ca60c93025e577af
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97231791"
---
# <a name="lthash_setgt"></a>&lt;hash_set&gt;

> [!NOTE]
> Этот заголовок устарел. Вместо него следует использовать [<unordered_set>](../standard-library/unordered-set.md).

Определяет шаблоны класса контейнера hash_set и hash_multiset и их вспомогательные шаблоны.

## <a name="syntax"></a>Синтаксис

```cpp
#include <hash_set>
```

## <a name="remarks"></a>Remarks

### <a name="operators"></a>Операторы

|Версия hash_set|Версия hash_multiset|Описание|
|-----------------------|----------------------------|-----------------|
|[operator! = (hash_set)](../standard-library/hash-set-operators.md#op_neq)|[operator!= (hash_multiset)](../standard-library/hash-set-operators.md#op_neq)|Проверяет неравенство объекта hash_set или hash_multiset слева от оператора объекту hash_set или hash_multiset справа от оператора.|
|[operator== (hash_set)](../standard-library/hash-set-operators.md#op_eq_eq)|[оператор = = (hash_multiset)](../standard-library/hash-set-operators.md#op_eq_eq)|Проверяет равенство объекта hash_set или hash_multiset слева от оператора объекту hash_set или hash_multiset справа от оператора.|

### <a name="specialized-template-functions"></a>Специализированные функции шаблонов

|Версия hash_set|Версия hash_multiset|Описание|
|-----------------------|----------------------------|-----------------|
|[swap (hash_set)](../standard-library/hash-set-functions.md#swap)|[Swap (hash_multiset)](../standard-library/hash-set-functions.md#swap_hash_multiset)|Меняет местами элементы двух объектов hash_set или hash_multiset.|

### <a name="classes"></a>Классы

|Класс|Описание|
|-|-|
|[Класс hash_compare](../standard-library/hash-compare-class.md)|Описывает объект, который может использоваться любым ассоциативным контейнером хэша — hash_map, hash_multimap, hash_set или hash_multiset — как объект параметра по умолчанию `Traits` для упорядочивания и хэширования элементов, содержащихся в них.|
|[Класс hash_set](../standard-library/hash-set-class.md)|Используется для хранения и быстрого извлечения данных из коллекции, в которой значения элементов должны быть уникальными и в которой они служат в качестве значений ключей.|
|[Класс hash_multiset](../standard-library/hash-multiset-class.md)|Используется для хранения и быстрого извлечения данных из коллекции, в которой значения элементов должны быть уникальными и в которой они служат в качестве значений ключей.|

## <a name="see-also"></a>См. также раздел

[Справочник по файлам заголовков](../standard-library/cpp-standard-library-header-files.md)\
[Безопасность потоков в стандартной библиотеке C++](../standard-library/thread-safety-in-the-cpp-standard-library.md)\
[Справочник по стандартной библиотеке C++](../standard-library/cpp-standard-library-reference.md)
