---
description: 'Дополнительные сведения о: Ошибка компилятора C3002'
title: Ошибка компилятора C3002
ms.date: 11/04/2016
f1_keywords:
- C3002
helpviewer_keywords:
- C3002
ms.assetid: 2d4241a7-c8eb-4d43-a128-dca255d137bc
ms.openlocfilehash: 00984b6d3ed0845dd532f82462d9c44f6893a846
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97326060"
---
# <a name="compiler-error-c3002"></a>Ошибка компилятора C3002

"имя1 имя2": несколько имен директивы OpenMP

Использование нескольких имен директивы запрещено.

При компиляции следующего примера возникнет ошибка C3002:

```c
// C3002.c
// compile with: /openmp
int main()
{
   #pragma omp parallel single   // C3002
}
```
