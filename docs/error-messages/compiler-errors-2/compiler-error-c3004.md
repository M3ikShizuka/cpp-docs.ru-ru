---
description: 'Дополнительные сведения о: Ошибка компилятора C3004'
title: Ошибка компилятора C3004
ms.date: 11/04/2016
f1_keywords:
- C3004
helpviewer_keywords:
- C3004
ms.assetid: 819c2b57-8366-4ca7-9135-1f0c5e5b6bb6
ms.openlocfilehash: 30737aca11b52fb8eaecc376c38211772442abf5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97326032"
---
# <a name="compiler-error-c3004"></a>Ошибка компилятора C3004

"предложение": предложение не допускается в директиве OpenMP "директива"

Предложение OpenMP используется в директиве, для которой оно не включено.

Следующий пример приводит к возникновению ошибки C3004:

```c
// C3004.c
// compile with: /openmp
int main()
{
   int x, y, z;

   // Shared clause not allowed for 'single' directive.
   #pragma omp single shared(x, y)   // C3004

   x = y;
}
```
