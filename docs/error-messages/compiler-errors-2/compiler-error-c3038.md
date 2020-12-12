---
description: 'Дополнительные сведения о: Ошибка компилятора C3038'
title: Ошибка компилятора C3038
ms.date: 11/04/2016
f1_keywords:
- C3038
helpviewer_keywords:
- C3038
ms.assetid: 140ada3e-5636-43ef-a4ee-22a9f66a771f
ms.openlocfilehash: bcc038ac21807b7d98ec98fa76004d658ef0216d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97270073"
---
# <a name="compiler-error-c3038"></a>Ошибка компилятора C3038

"переменная": переменная в предложении private не может быть редукционной переменной в охватывающем контексте

Переменная, используемая в предложении [reduction](../../parallel/openmp/reference/openmp-clauses.md#reduction) параллельной директивы, не может быть указана в предложении [private](../../parallel/openmp/reference/openmp-clauses.md#private-openmp) в директиве распределения рабочей нагрузки, которая привязывается к параллельной конструкции.

Следующий пример приводит к возникновению ошибки C3038:

```cpp
// C3038.cpp
// compile with: /openmp /c
int g_i, g_i2;

int main() {
   int i;

   #pragma omp parallel reduction(+: g_i)
   {
      #pragma omp for private(g_i)   // C3038
      // try the following line instead
      // #pragma omp for private(g_i2)
      for (i = 0; i < 10; ++i)
         g_i += i;
   }
}
```
