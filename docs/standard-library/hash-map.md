---
description: 'Дополнительные сведения: &lt; hash_map&gt;'
title: '&lt;hash_map&gt;'
ms.date: 01/18/2018
f1_keywords:
- <hash_map>
helpviewer_keywords:
- hash_map header
ms.openlocfilehash: 9d8274958a0f6b89892ec2c1c70080cd090d1c03
ms.sourcegitcommit: 118e4ad82c0f1c9ac120f105d84224e5fe4cef28
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/12/2021
ms.locfileid: "98125978"
---
# <a name="lthash_mapgt"></a>&lt;hash_map&gt;

> [!NOTE]
> Этот заголовок устарел. Альтернативой является [\<unordered_map>](unordered-map.md) .

Определяет шаблоны класса контейнера hash_map и hash_multimap и их вспомогательные шаблоны.

## <a name="syntax"></a>Синтаксис

```cpp
#include <hash_map>
```

### <a name="operators"></a>Операторы

|Версия hash_map|Версия hash_multimap|Описание|
|-----------------------|----------------------------|-----------------|
|[operator!= (hash_map)](hash-map-operators.md#op_neq)|[operator! = (hash_multimap)](hash-map-operators.md#op_neq_mm)|Проверяет неравенство объекта hash_map или hash_multimap слева от оператора объекту hash_map или hash_multimap справа от оператора.|
|[оператор = = (hash_map)](hash-map-operators.md#op_eq_eq)|[operator== (hash_multimap)](hash-map-operators.md#op_eq_eq_mm)|Проверяет равенство объекта hash_map или hash_multimap слева от оператора объекту hash_map или hash_multimap справа от оператора.|

### <a name="specialized-template-functions"></a>Специализированные функции шаблонов

|Версия hash_map|Версия hash_multimap|Описание|
|-----------------------|----------------------------|-----------------|
|[swap (hash_map)](hash-map-class.md#swap)|[swap (hash_multimap)](hash-multimap-class.md#swap)|Меняет местами элементы двух объектов hash_map или hash_multimap.|

### <a name="classes"></a>Классы

|Класс|Описание|
|-|-|
|[Класс hash_compare](hash-compare-class.md)|Описывает объект, который может использоваться любым ассоциативным контейнером хэша — hash_map, hash_multimap, hash_set или hash_multiset — как объект параметра по умолчанию `Traits` для упорядочивания и хэширования элементов, содержащихся в них.|
|[Класс value_compare](value-compare-class.md)|Предоставляет объект функции, который может сравнивать элементы hash_map путем сравнения значения ключей для определения относительного порядка в hash_map.|
|[Класс hash_map](hash-map-class.md)|Используется для хранения и быстрого считывания данных из коллекции, в которой каждый элемент — это пара, которая имеет отсортированный уникальный ключ и связанное с ним значение.|
|[Класс hash_multimap](hash-multimap-class.md)|Используется для хранения и быстрого считывания данных из коллекции, в которой каждый элемент — это пара, которая имеет ключ, значение которого не должно быть уникальным, и связанное с ним значение.|

## <a name="requirements"></a>Требования

**Заголовок:**\<hash_map>

**Пространство имен:** stdext

## <a name="see-also"></a>См. также раздел

[Справочник по файлам заголовков](cpp-standard-library-header-files.md)\
[Безопасность потоков в стандартной библиотеке C++](thread-safety-in-the-cpp-standard-library.md)\
[Справочник по стандартной библиотеке C++](cpp-standard-library-reference.md)
