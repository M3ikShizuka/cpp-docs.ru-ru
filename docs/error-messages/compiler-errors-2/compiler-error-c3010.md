---
description: 'Дополнительные сведения о: Ошибка компилятора C3010'
title: Ошибка компилятора C3010
ms.date: 11/04/2016
f1_keywords:
- C3010
helpviewer_keywords:
- C3010
ms.assetid: e959d038-bba6-432a-9c0a-0470474de7d9
ms.openlocfilehash: 50467ad1cb03255cbb5ef008e2ac2897de4a6a5c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97305316"
---
# <a name="compiler-error-c3010"></a>Ошибка компилятора C3010

"метка": переход из структурированного блока OpenMP запрещен

Код не может переходить в блок OpenMP или из этого блока.

Следующий пример приводит к возникновению ошибки C3010.

```c
// C3010.c
// compile with: /openmp
int main() {
   #pragma omp parallel
   {
      #pragma omp parallel
      {
         goto lbl3;
      }
   }
   lbl3:;   // C3010
}
```
