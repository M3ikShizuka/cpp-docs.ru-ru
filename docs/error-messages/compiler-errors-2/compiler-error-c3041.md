---
description: 'Дополнительные сведения о: Ошибка компилятора C3041'
title: Ошибка компилятора C3041
ms.date: 11/04/2016
f1_keywords:
- C3041
helpviewer_keywords:
- C3041
ms.assetid: 9df1ae44-3ac7-4c6c-899f-f35ffe7ccf0d
ms.openlocfilehash: ce4a0b1dbbcc0dc83b84c25afd4acf43fa0af687
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97269939"
---
# <a name="compiler-error-c3041"></a>Ошибка компилятора C3041

"переменная": переменная в предложении copyprivate должна быть частной в охватывающем контексте

Переменная, передаваемая в предложение [copyprivate](../../parallel/openmp/reference/openmp-clauses.md#copyprivate) , не может быть общей в охватывающем контексте.

Следующий пример приводит к возникновению ошибки C3041:

```cpp
// C3041.cpp
// compile with: /openmp /c
#include "omp.h"
double d;
int main() {
   #pragma omp parallel shared(d)
   // try the following line instead
   // #pragma omp parallel private(d)
   {
      // or don't make d copyprivate
      #pragma omp single copyprivate(d)   // C3041
      {
      }
   }
}
```
