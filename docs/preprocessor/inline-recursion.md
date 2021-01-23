---
description: Дополнительные сведения об pragma директиве inline_recursion в Microsoft C/C++
title: inline_recursion pragma
ms.date: 01/22/2021
f1_keywords:
- inline_recursion_CPP
- vc-pragma.inline_recursion
helpviewer_keywords:
- pragma, inline_recursion
- inline_recursion pragma
no-loc:
- pragma
ms.openlocfilehash: b4e377d4c97c46a20e44a2c41f872a8762cdea4d
ms.sourcegitcommit: a26a66a3cf479e0e827d549a9b850fad99b108d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/22/2021
ms.locfileid: "98713562"
---
# <a name="inline_recursion-no-locpragma"></a>`inline_recursion` pragma

Управляет развертыванием встроенного кода непосредственных или взаимных рекурсивных вызовов функций.

## <a name="syntax"></a>Синтаксис

> **`#pragma inline_recursion(`** [ { **`on`** | **`off`** } ] **`)`**

## <a name="remarks"></a>Примечания

Используйте этот pragma параметр для управления функциями, помеченными как [`inline`](../cpp/inline-functions-cpp.md) [`__inline`](../cpp/inline-functions-cpp.md) функции и или, которые компилятор автоматически расширяет при **`/Ob2`** выборе параметра. При использовании этого параметра pragma [`/Ob`](../build/reference/ob-inline-function-expansion.md) параметр компилятора имеет значение 1 или 2. Состояние по умолчанию для **`inline_recursion`** — Off. Это pragma вступает в силу при первом вызове функции после pragma рассмотрения и не влияет на определение функции.

**`inline_recursion`** pragma Управляет развертыванием рекурсивных функций. Если **`inline_recursion`** параметр имеет значение OFF и если встроенная функция вызывает саму себя прямо или косвенно, функция разворачивается только один раз. Если **`inline_recursion`** параметр имеет значение ON, функция разворачивается несколько раз до тех пор, пока не достигнет значения, заданного параметром [`inline_depth`](../preprocessor/inline-depth.md) pragma , значения по умолчанию для рекурсивных функций, определяемых параметром `inline_depth` pragma , или предела емкости.

## <a name="see-also"></a>См. также раздел

[Директивы pragma и `__pragma` `_Pragma` Ключевые слова и](./pragma-directives-and-the-pragma-keyword.md)\
[`inline_depth`](../preprocessor/inline-depth.md)\
[`/Ob` (Расширение встроенной функции)](../build/reference/ob-inline-function-expansion.md)
