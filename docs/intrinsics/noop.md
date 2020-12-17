---
description: 'Дополнительные сведения о встроенных функциях Microsoft C/C++: __noop'
title: __noop
ms.date: 12/16/2020
f1_keywords:
- __noop_cpp
- __noop
helpviewer_keywords:
- __noop keyword [C++]
ms.assetid: 81ac6e97-7bf8-496b-b3c4-fd02837573e5
ms.openlocfilehash: 5fd300ca8d68305a12e6b5540be05aa60a042a44
ms.sourcegitcommit: 387ce22a3b0137f99cbb856a772b5a910c9eba99
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "97645089"
---
# `__noop`

 **`__noop`** Встроенная функция Майкрософт указывает, что функцию следует игнорировать. Список аргументов анализируется, но для аргументов не создается код. Компилятор рассматривает аргументы как упоминаемые в целях C4100 предупреждений компилятора и аналогичного анализа. `__noop`Встроенное значение предназначено для использования в функциях глобальной отладки, принимающих переменное число аргументов.

Компилятор преобразует **`__noop`** встроенное значение в 0 во время компиляции.

## <a name="example"></a>Пример

В следующем коде показано, как можно использовать **`__noop`** .

```cpp
// compiler_intrinsics__noop.cpp
// compile using: cl /EHsc /W4 compiler_intrinsics__noop.cpp
// compile with or without /DDEBUG
#include <stdio.h>

#if DEBUG
   #define PRINT   printf_s
#else
   #define PRINT   __noop
#endif

#define IGNORE(x) { __noop(x); }

int main(int argv, char ** argc)
{
   IGNORE(argv);
   IGNORE(argc);
   PRINT("\nDEBUG is defined\n");
}
```

## <a name="see-also"></a>См. также раздел

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)\
[Ключевые слова](../cpp/keywords-cpp.md)
