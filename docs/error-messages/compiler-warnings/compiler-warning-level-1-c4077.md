---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4077'
title: Предупреждение компилятора (уровень 1) C4077
ms.date: 11/04/2016
f1_keywords:
- C4077
helpviewer_keywords:
- C4077
ms.assetid: c2d28805-b33f-41ad-afba-33b3f788c649
ms.openlocfilehash: 96e611db6d36dfa62d96561deb2f4c4d57638c72
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97208714"
---
# <a name="compiler-warning-level-1-c4077"></a>Предупреждение компилятора (уровень 1) C4077

неизвестный параметр check_stack

Старая форма прагмы **check_stack** используется с неизвестным аргументом. Аргумент должен быть `+`, `-`, `(on)`, `(off)`или быть пустым.

Компилятор игнорирует эту прагму и оставляет проверку стека неизмененной.

## <a name="example"></a>Пример

```cpp
// C4077.cpp
// compile with: /W1 /LD
#pragma check_stack yes // C4077
#pragma check_stack +    // Correct old form
#pragma check_stack (on) // Correct new form
```
