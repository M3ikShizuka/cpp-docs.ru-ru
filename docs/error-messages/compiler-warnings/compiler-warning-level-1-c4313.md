---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4313'
title: Предупреждение компилятора (уровень 1) C4313
ms.date: 11/04/2016
f1_keywords:
- C4313
helpviewer_keywords:
- C4313
ms.assetid: bcf64191-e2cf-452e-97b4-423fcec2d07c
ms.openlocfilehash: dbf609ebac3e94cb7f49494c815cb40414c9b510
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97311660"
---
# <a name="compiler-warning-level-1-c4313"></a>Предупреждение компилятора (уровень 1) C4313

function: описатель формата в строке формата конфликтует с количеством аргументов типа type

Существует конфликт между указанным форматом и переданным значением. Например, вы передали 64-разрядный параметр неполному описателю формата %d, который ожидает 32-разрядное целое число. Это предупреждение действует только при компиляции кода для 64-разрядных сред.

## <a name="example"></a>Пример

В следующем примере кода возникает ошибка C4313 при компиляции для 64-разрядных сред.

```cpp
// C4313.cpp
// Compile by using: cl /W1 C4313.cpp
#include <stdio.h>
int main() {
   int * pI = 0;
   printf("%d", pI);   // C4313 on 64-bit platform code
   // Try one of the following lines instead:
   // printf("%p\n", pI);
   // printf("%Id\n", pI);   // %I64d expects 64-bits of information
}
```
