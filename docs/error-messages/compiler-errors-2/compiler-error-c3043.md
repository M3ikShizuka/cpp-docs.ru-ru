---
description: 'Дополнительные сведения о: Ошибка компилятора C3043'
title: Ошибка компилятора C3043
ms.date: 11/04/2016
f1_keywords:
- C3043
helpviewer_keywords:
- C3043
ms.assetid: 0ef55e63-e82b-48eb-9d44-690950ac34c6
ms.openlocfilehash: e63c5bd5857b0b962b8bee464eb77d31e1b1edd1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97269891"
---
# <a name="compiler-error-c3043"></a>Ошибка компилятора C3043

Директиву OpenMP "critical" нельзя вложить в директиву critical с тем же именем

Директиву [critical](../../parallel/openmp/reference/openmp-directives.md#critical) нельзя вложить в директиву `critical` с тем же именем.

Следующий пример приводит к возникновению ошибки C3043:

```cpp
// C3043.cpp
// compile with: /openmp /c
#include "omp.h"

int main() {
   int n1 = 1, n2 = 2, n3 = 3;

   #pragma omp parallel
   {
      ++n2;

      #pragma omp critical(MyTest)
      {
         ++n2;

         #pragma omp critical(MyTest)   // C3043
         // try the following line instead
         // #pragma omp critical(MyTest2)
         {
            ++n3;
         }
      }
   }
}
```
