---
description: 'Дополнительные сведения о: Ошибка компилятора C3001'
title: Ошибка компилятора C3001
ms.date: 11/04/2016
f1_keywords:
- C3001
helpviewer_keywords:
- C3001
ms.assetid: d0e03478-1b44-47e5-8f5b-70415fa1f8bc
ms.openlocfilehash: cf8acec3fb95553787e14968b9ce3e608da83916
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97253602"
---
# <a name="compiler-error-c3001"></a>Ошибка компилятора C3001

"текст_ошибки": требуется имя директивы OpenMP

За директивой pragma `omp` должна следовать директива.

Следующий пример приводит к возникновению ошибки C3001:

```c
// C3001.c
// compile with: /openmp
int main()
{
   #pragma omp   // C3001 missing token
}
```
