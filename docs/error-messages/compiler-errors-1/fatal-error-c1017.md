---
description: 'Дополнительные сведения о: Неустранимая ошибка C1017'
title: Неустранимая ошибка C1017
ms.date: 11/04/2016
f1_keywords:
- C1017
helpviewer_keywords:
- C1017
ms.assetid: 5542e604-599d-4e36-8f83-1d454c5753c9
ms.openlocfilehash: a36a5cb11b10ca3ecca00d0379595060918d6a45
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97262390"
---
# <a name="fatal-error-c1017"></a>Неустранимая ошибка C1017

недопустимое константное выражение целого типа

Выражение в `#if` директиве не существовало или не вычисляется как константа.

Константы, определенные с помощью `#define` , должны иметь значения, вычисляемые в целочисленную константу, если они используются в `#if` `#elif` `#else` директиве, или.

Следующий пример приводит к возникновению ошибки C1017:

```cpp
// C1017.cpp
#define CONSTANT_NAME "YES"
#if CONSTANT_NAME   // C1017
#endif
```

Возможное решение:

```cpp
// C1017b.cpp
// compile with: /c
#define CONSTANT_NAME 1
#if CONSTANT_NAME
#endif
```

Поскольку `CONSTANT_NAME` вычисляет строку, а не целое число, `#if` директива создает неустранимую ошибку C1017.

В других случаях препроцессор вычисляет неопределенную константу как ноль. Это может привести к непредвиденным результатам, как показано в следующем примере. `YES` не определено, поэтому принимает значение 0. Выражение `#if` `CONSTANT_NAME` принимает значение false, а код, используемый для `YES` , удаляется препроцессором. `NO` значение также не определено (ноль), поэтому `#elif` `CONSTANT_NAME==NO` вычисляется как true ( `0 == 0` ), что приводит к тому, что препроцессор оставляет код в `#elif` части оператора — точно так же, как и в противоположном поведении.

```cpp
// C1017c.cpp
// compile with: /c
#define CONSTANT_NAME YES
#if CONSTANT_NAME
   // Code to use on YES...
#elif CONSTANT_NAME==NO
   // Code to use on NO...
#endif
```

Чтобы точно увидеть, как компилятор обрабатывает директивы препроцессора, используйте [/p](../../build/reference/p-preprocess-to-a-file.md), [/e](../../build/reference/e-preprocess-to-stdout.md)или [/EP](../../build/reference/ep-preprocess-to-stdout-without-hash-line-directives.md).
