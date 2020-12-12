---
description: 'Дополнительные сведения о: inline_recursion pragma'
title: Прагма inline_recursion
ms.date: 08/29/2019
f1_keywords:
- inline_recursion_CPP
- vc-pragma.inline_recursion
helpviewer_keywords:
- pragmas, inline_recursion
- inline_recursion pragma
ms.assetid: cfef5791-63b7-45ac-9574-623747b9b9c9
ms.openlocfilehash: 1688eb724a9a76ce3f173c7f9eac7d52032fbe13
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97236377"
---
# <a name="inline_recursion-pragma"></a>Прагма inline_recursion

Управляет развертыванием встроенного кода непосредственных или взаимных рекурсивных вызовов функций.

## <a name="syntax"></a>Синтаксис

> **inline_recursion #pragma (** [{ **On**  |  **Off** }] **)**

## <a name="remarks"></a>Комментарии

Используйте эту директиву pragma для управления функциями, помеченными как [встроенные](../cpp/inline-functions-cpp.md) и [__inline](../cpp/inline-functions-cpp.md) или функциями, которые компилятор автоматически расширяет при `/Ob2` выборе параметра. Для использования этой директивы pragma требуется параметр компилятора [/Ob](../build/reference/ob-inline-function-expansion.md) , имеющий значение 1 или 2. Состояние по умолчанию для **inline_recursion** — Off. Эта директива pragma вступает в силу при первом вызове функции после того, как директива pragma будет показана и не влияет на определение функции.

Директива pragma **inline_recursion** определяет, как разворачиваются рекурсивные функции. Если **inline_recursion** имеет значение OFF и если встроенная функция вызывает саму себя прямо или косвенно, функция разворачивается только один раз. Если **inline_recursion** имеет значение ON, функция разворачивается несколько раз до тех пор, пока не достигнет значения, установленного с помощью директивы pragma [inline_depth](../preprocessor/inline-depth.md) , значения по умолчанию для рекурсивных функций, определенных `inline_depth` директивой pragma, или предела емкости.

## <a name="see-also"></a>См. также раздел

[Директивы pragma и ключевое слово __pragma](../preprocessor/pragma-directives-and-the-pragma-keyword.md)\
[inline_depth](../preprocessor/inline-depth.md)\
[/OB (расширение встроенных функций)](../build/reference/ob-inline-function-expansion.md)
