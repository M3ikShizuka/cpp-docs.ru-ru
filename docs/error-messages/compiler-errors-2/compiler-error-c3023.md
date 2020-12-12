---
description: 'Дополнительные сведения о: Ошибка компилятора C3023'
title: Ошибка компилятора C3023
ms.date: 11/04/2016
f1_keywords:
- C3023
helpviewer_keywords:
- C3023
ms.assetid: 89dcce98-3cd7-4931-a50f-87df1d2ebc9b
ms.openlocfilehash: e9cd560610327afe1dabc2b6899d1e0290779ded
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97174342"
---
# <a name="compiler-error-c3023"></a>Ошибка компилятора C3023

"значение": непредвиденный токен в аргументе предложения OpenMP "предложение"

Значения, передаваемые в предложение, недопустимы.

Следующий пример приводит к возникновению ошибки C3023:

```cpp
// C3023.cpp
// compile with: /openmp /link vcomps.lib
#include <stdio.h>
#include "omp.h"

int main() {
   int i;

   #pragma omp parallel for schedule(dynamic 10)   // C3023
   for (i = 0; i < 10; ++i) ;

   #pragma omp parallel for schedule(dynamic;10)   // C3023
   for (i = 0; i < 10; ++i) ;

   // OK
   #pragma omp parallel for schedule(dynamic, 10)
   for (i = 0; i < 10; ++i)
   ;
}
```
