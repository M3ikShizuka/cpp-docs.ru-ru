---
description: 'Дополнительные сведения: _SECURE_SCL'
title: _SECURE_SCL
ms.date: 11/04/2016
f1_keywords:
- _SECURE_SCL
helpviewer_keywords:
- _SECURE_SCL
ms.assetid: 4ffbc788-cc12-4c6a-8cd7-490081675086
ms.openlocfilehash: 1a0e32ada449709a60eb601138ce0bb8b7ae9123
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97197105"
---
# <a name="_secure_scl"></a>_SECURE_SCL

Этот макрос, заменяемый [_ITERATOR_DEBUG_LEVEL](../standard-library/iterator-debug-level.md), определяет, включены ли [Проверяемые итераторы](../standard-library/checked-iterators.md). По умолчанию проверяемые итераторы включены в отладочных сборках и отключены в окончательных сборках.

> [!IMPORTANT]
> Прямое использование макроса _SECURE_SCL является устаревшим. Вместо этого используйте _ITERATOR_DEBUG_LEVEL, чтобы управлять установленными параметрами итератора. Дополнительные сведения см. в разделе [_ITERATOR_DEBUG_LEVEL](../standard-library/iterator-debug-level.md).

## <a name="remarks"></a>Комментарии

Если проверяемые итераторы включены, небезопасный итератор может вызвать ошибку во время выполнения и программа будет завершена. Чтобы включить Проверяемые итераторы, установите _ITERATOR_DEBUG_LEVEL в значение 1 или 2. Это эквивалентно параметру _SECURE_SCL, равному 1, или включенному.

```cpp
#define _ITERATOR_DEBUG_LEVEL 1
```

Чтобы отключить Проверяемые итераторы, установите _ITERATOR_DEBUG_LEVEL в значение 0. Это эквивалентно значению параметра _SECURE_SCL 0 или отключенному.

```cpp
#define _ITERATOR_DEBUG_LEVEL 0
```

Сведения о том, как отключить предупреждения о проверяемых итераторах, см. в разделе [_SCL_SECURE_NO_WARNINGS](../standard-library/scl-secure-no-warnings.md).

## <a name="see-also"></a>См. также раздел

[_ITERATOR_DEBUG_LEVEL](../standard-library/iterator-debug-level.md)\
[Проверенные итераторы](../standard-library/checked-iterators.md)\
[Поддержка итератора отладки](../standard-library/debug-iterator-support.md)\
[Надежные библиотеки: Стандартная библиотека C++](../standard-library/safe-libraries-cpp-standard-library.md)
