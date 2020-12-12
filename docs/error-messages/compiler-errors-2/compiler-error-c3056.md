---
description: 'Дополнительные сведения о: Ошибка компилятора C3056'
title: Ошибка компилятора C3056
ms.date: 11/04/2016
f1_keywords:
- C3056
helpviewer_keywords:
- C3056
ms.assetid: 9500173d-870b-49b3-8e88-0ee93586d19a
ms.openlocfilehash: d934221c4501256eb4bfd604bcc04534268de3fa
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97269540"
---
# <a name="compiler-error-c3056"></a>Ошибка компилятора C3056

"символ": символ не находится в одной области с директивой threadprivate

Символ, используемый в предложении [threadprivate](../../parallel/openmp/reference/openmp-directives.md#threadprivate) , должен находиться в той же области, что и предложение `threadprivate` .

В следующем примере возникает ошибка C3056.

```cpp
// C3056.cpp
// compile with: /openmp
int x, y;
void test() {
   #pragma omp threadprivate(x, y)   // C3056
   #pragma omp parallel copyin(x, y)
   {
      x = y;
   }
}
```

Возможное решение:

```cpp
// C3056b.cpp
// compile with: /openmp /LD
int x, y;
#pragma omp threadprivate(x, y)
void test() {
   #pragma omp parallel copyin(x, y)
   {
      x = y;
   }
}
```
