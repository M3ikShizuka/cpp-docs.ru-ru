---
description: 'Дополнительные сведения о: Ошибка компилятора C3030'
title: Ошибка компилятора C3030
ms.date: 11/04/2016
f1_keywords:
- C3030
helpviewer_keywords:
- C3030
ms.assetid: de92fd7e-29ba-46e8-b43b-f4b985cd74de
ms.openlocfilehash: 58589bdb58685c3a0d21f362d1f625c3aeecba2e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97174173"
---
# <a name="compiler-error-c3030"></a>Ошибка компилятора C3030

"переменная": переменная в предложении или директиве "reduction" не может быть ссылочного типа

Вы можете передавать параметры значений только в некоторые предложения, такие как предложение reduction.

Следующий пример приводит к возникновению ошибки C3030:

```cpp
// C3030.cpp
// compile with: /openmp /link vcomps.lib
#include "omp.h"

void test(int &r) {
   #pragma omp parallel reduction(+ : r)   // C3030
      ;
}

void test2(int r) {
   #pragma omp parallel reduction(+ : r)   // OK
      ;
}

int main(int argc, char** argv) {
   int& r = *((int*)argv);
   int s = *((int*)argv);

   #pragma omp parallel reduction(+ : r)   // C3030
      ;

   #pragma omp parallel reduction(+ : s)   // OK
      ;
}
```
