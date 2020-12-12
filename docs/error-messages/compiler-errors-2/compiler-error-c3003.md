---
description: 'Дополнительные сведения о: Ошибка компилятора C3003'
title: Ошибка компилятора C3003
ms.date: 11/04/2016
f1_keywords:
- C3003
helpviewer_keywords:
- C3003
ms.assetid: 22e74f99-bb7f-4518-ab0d-934d5d49bcc7
ms.openlocfilehash: 1bed98ebd9e0a383700583e1e23e0a977cb6e3fc
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97326047"
---
# <a name="compiler-error-c3003"></a>Ошибка компилятора C3003

"директива": имя директивы OpenMP не допускается после предложений директивы

Имя директивы OpenMP не может следовать после предложения директивы OpenMP.

Следующий пример приводит к возникновению ошибки C3003.

```c
// C3003.c
// compile with: /openmp
int main()
{
   int x, y, z;
   #pragma omp parallel shared(x, y, z) for   // C3003
}
```
