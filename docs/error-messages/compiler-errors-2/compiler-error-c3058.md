---
description: 'Дополнительные сведения о: Ошибка компилятора C3058'
title: Ошибка компилятора C3058
ms.date: 11/04/2016
f1_keywords:
- C3058
helpviewer_keywords:
- C3058
ms.assetid: 669d08c8-0b58-4351-88aa-c6e6e1af481c
ms.openlocfilehash: 9a7c4c3fa4fd8186055985ff66caa3ffd0c4f081
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97269462"
---
# <a name="compiler-error-c3058"></a>Ошибка компилятора C3058

"символ": символ не объявлен как threadprivate до его использования в предложении copyin

Символ нужно сначала объявить как [threadprivate](../../parallel/openmp/reference/openmp-directives.md#threadprivate) перед тем, как его можно будет использовать в предложении [copyin](../../parallel/openmp/reference/openmp-clauses.md#copyin) .

При компиляции следующего примера возникнет ошибка C3058:

```cpp
// C3058.cpp
// compile with: /openmp
int x, y, z;
#pragma omp threadprivate(x, z)

void test() {
   #pragma omp parallel copyin(x, y)   // C3058
   {
   }
}
```

Возможное решение:

```cpp
// C3058b.cpp
// compile with: /openmp /LD
int x, y, z;
#pragma omp threadprivate(x, y)

void test() {
   #pragma omp parallel copyin(x, y)
   {
   }
}
```
