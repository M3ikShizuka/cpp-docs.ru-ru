---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 4) C4938'
title: Предупреждение компилятора (уровень 4) C4938
ms.date: 11/04/2016
f1_keywords:
- C4938
helpviewer_keywords:
- C4938
ms.assetid: 6acac81a-9d23-465e-b700-ed4b6e8edcd0
ms.openlocfilehash: 3b327581b0eb790e74d6fddc2bca1e027f40d89e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97234596"
---
# <a name="compiler-warning-level-4-c4938"></a>Предупреждение компилятора (уровень 4) C4938

"переменная": переменная сокращения формата с плавающей точкой может привести к несогласованным результатам при использовании /fp:strict или #pragma fenv_access

Не следует использовать [/fp: strict](../../build/reference/fp-specify-floating-point-behavior.md) или [fenv_access](../../preprocessor/fenv-access.md) с сокращениями чисел с плавающей запятой OpenMP, так как сумма вычисляется в другом порядке. Таким образом, результаты могут отличаться от результатов вычислений без использования параметра /openmp.

При компиляции следующего примера будет выдано предупреждение C4938:

```cpp
// C4938.cpp
// compile with: /openmp /W4 /fp:strict /c
// #pragma fenv_access(on)
extern double *a;

double test(int first, int last) {
   double sum = 0.0;
   #pragma omp parallel for reduction(+: sum)   // C4938
   for (int i = first ; i <= last ; ++i)
      sum += a[i];
   return sum;
}
```

Без явной параллелизации сумма вычисляется следующим образом:

```
sum = a[first] + a[first + 1] + ... + a[last];
```

С явной параллелизацией (и двумя потоками) сумма вычисляется следующим образом:

```
sum1 = a[first] + ... a[first + last / 2];
sum2 = a[(first + last / 2) + 1] + ... a[last];
sum = sum1 + sum2;
```
