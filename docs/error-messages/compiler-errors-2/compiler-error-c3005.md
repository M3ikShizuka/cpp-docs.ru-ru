---
description: 'Дополнительные сведения о: Ошибка компилятора C3005'
title: Ошибка компилятора C3005
ms.date: 11/04/2016
f1_keywords:
- C3005
helpviewer_keywords:
- C3005
ms.assetid: 30bad565-e79f-4c3f-82cb-a74bd0baab8f
ms.openlocfilehash: df9e0c94aa0ba47e1c2f63858419c15881f9bd74
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97272426"
---
# <a name="compiler-error-c3005"></a>Ошибка компилятора C3005

"текст_ошибки": непредвиденная лексема в директиве OpenMP "директива"

Директива OpenMP сформирована неправильно.

В следующем примере возникает ошибка C3005:

```c
// C3005.c
// compile with: /openmp
int main()
{
   #pragma omp parallel + for   // C3005
}
```

Ошибка C3005 также может возникать, если поместить открывающую фигурную скобку в одной строке с директивой pragma.

```c
// C3005b.c
// compile with: /openmp
int main() {
   #pragma omp parallel {   // C3005 put open brace on next line
   lbl2:;
   }
   goto lbl2;
}
```
