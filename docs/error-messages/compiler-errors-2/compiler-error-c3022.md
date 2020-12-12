---
description: 'Дополнительные сведения о: Ошибка компилятора C3022'
title: Ошибка компилятора C3022
ms.date: 11/04/2016
f1_keywords:
- C3022
helpviewer_keywords:
- C3022
ms.assetid: 9f1d444c-6c6e-48d9-9346-69128390aa33
ms.openlocfilehash: 66d9fa5e4eec93a1fcb4182c8c4e8672c586aa76
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97174368"
---
# <a name="compiler-error-c3022"></a>Ошибка компилятора C3022

"предложение": недопустимый вид расписания "значение" в директиве OpenMP "директива"

В предложение было передано неподдерживаемое значение.

Следующий пример приводит к возникновению ошибки C3022:

```cpp
// C3022.cpp
// compile with: /openmp /link vcomps.lib
#include <stdio.h>
#include "omp.h"

int main() {
   int i;

   #pragma omp parallel for schedule(10)   // C3022
   for (i = 0; i < 10; ++i) ;

   #pragma omp parallel for schedule(x)   // C3022
   for (i = 0; i < 10; ++i) ;

   // OK
   #pragma omp parallel for schedule(runtime)
   for (i = 0; i < 10; ++i)
   ;
}
```
