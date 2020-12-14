---
description: 'Дополнительные сведения: _HAS_ITERATOR_DEBUGGING'
title: _HAS_ITERATOR_DEBUGGING
ms.date: 11/04/2016
f1_keywords:
- _HAS_ITERATOR_DEBUGGING
helpviewer_keywords:
- _HAS_ITERATOR_DEBUGGING
ms.assetid: 90077dbb-8a76-4963-83a6-29f4854007a8
ms.openlocfilehash: ee1765739624fe7c6fccd41ff84f455d5f90cc42
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97231996"
---
# <a name="_has_iterator_debugging"></a>_HAS_ITERATOR_DEBUGGING

Этот макрос, который был заменен макросом [_ITERATOR_DEBUG_LEVEL](../standard-library/iterator-debug-level.md), определяет, включена ли функция отладки итераторов в отладочной сборке. По умолчанию отладка итераторов включена в отладочных сборках и отключена в окончательных сборках. Дополнительные сведения см. в разделе [Поддержка итераторов отладки](../standard-library/debug-iterator-support.md).

> [!IMPORTANT]
> Прямое использование макроса _HAS_ITERATOR_DEBUGGING является устаревшим. Вместо этого используйте _ITERATOR_DEBUG_LEVEL для управления параметрами отладки итератора. Дополнительные сведения см. в разделе [_ITERATOR_DEBUG_LEVEL](../standard-library/iterator-debug-level.md).

## <a name="remarks"></a>Комментарии

Чтобы включить отладку итераторов в отладочных сборках, задайте для _ITERATOR_DEBUG_LEVEL значение 2. Это эквивалентно параметру _HAS_ITERATOR_DEBUGGING, равному 1, или включенному.

```cpp
#define _ITERATOR_DEBUG_LEVEL 2
```

_ITERATOR_DEBUG_LEVEL не может быть задано равным 2 (а _HAS_ITERATOR_DEBUGGING не может иметь значение 1) в розничных сборках.

Чтобы отключить итераторы отладки в отладочных сборках, установите _ITERATOR_DEBUG_LEVEL в значение 0 или 1. Это эквивалентно значению параметра _HAS_ITERATOR_DEBUGGING 0 или отключенному.

```cpp
#define _ITERATOR_DEBUG_LEVEL 0
```

## <a name="see-also"></a>См. также раздел

[_ITERATOR_DEBUG_LEVEL](../standard-library/iterator-debug-level.md)\
[Поддержка итератора отладки](../standard-library/debug-iterator-support.md)\
[Проверенные итераторы](../standard-library/checked-iterators.md)\
[Надежные библиотеки: Стандартная библиотека C++](../standard-library/safe-libraries-cpp-standard-library.md)
