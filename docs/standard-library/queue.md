---
description: 'Подробнее о: &lt; очередь&gt;'
title: '&lt;queue&gt;'
ms.date: 11/04/2016
f1_keywords:
- <queue>
helpviewer_keywords:
- queue header
ms.assetid: 24fcf350-eb0e-48cf-9fef-978be1aeda1f
ms.openlocfilehash: f219cf3f457ed43eb2d9ca1658244a40ceacb265
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97327588"
---
# <a name="ltqueuegt"></a>&lt;queue&gt;

Определяет шаблоны классов priority_queue и очереди, а также несколько вспомогательных шаблонов.

## <a name="requirements"></a>Требования

**Заголовок:**\<queue>

**Пространство имен:** std

> [!NOTE]
> \<queue>Библиотека также использует `#include <initializer_list>` инструкцию.

## <a name="members"></a>Элементы

### <a name="operators"></a>Операторы

|Имя|Описание|
|-|-|
|[operator! =](../standard-library/queue-operators.md#op_neq)|Проверяет неравенство объекта queue слева от оператора объекту queue справа от оператора.|
|[Оператор<](../standard-library/queue-operators.md#op_lt)|Проверяет, меньше ли объект queue слева от оператора, чем объект queue справа от оператора.|
|[станции\<=](../standard-library/queue-operators.md#op_gt_eq)|Проверяет, меньше ли объект queue слева от оператора, чем объект queue справа от оператора, или равен ему.|
|[Оператор = =](../standard-library/queue-operators.md#op_eq_eq)|Проверяет равенство объекта queue слева от оператора объекту queue справа от оператора.|
|[Оператор>](../standard-library/queue-operators.md#op_gt)|Проверяет, больше ли объект queue слева от оператора, чем объект queue справа от оператора.|
|[Оператор>=](../standard-library/queue-operators.md#op_gt_eq)|Проверяет, больше ли объект queue слева от оператора, чем объект queue справа от оператора, или равен ему.|

### <a name="classes"></a>Классы

|name|Описание|
|-|-|
|[Класс Queue](../standard-library/queue-class.md)|Класс адаптера контейнера шаблона, который предоставляет ограничение функциональности, ограничивая доступ к переднему и заднему элементам некоторого базового типа контейнера.|
|[Класс priority_queue](../standard-library/priority-queue-class.md)|Класс адаптера контейнера шаблона, который предоставляет ограничение функциональности, ограничивая доступ к верхнему элементу некоторого базового типа контейнера, который всегда является самым большим.|

## <a name="see-also"></a>См. также раздел

[Справочник по файлам заголовков](../standard-library/cpp-standard-library-header-files.md)\
[Безопасность потоков в стандартной библиотеке C++](../standard-library/thread-safety-in-the-cpp-standard-library.md)\
[Справочник по стандартной библиотеке C++](../standard-library/cpp-standard-library-reference.md)
