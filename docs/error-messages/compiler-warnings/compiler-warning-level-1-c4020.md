---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4020'
title: Предупреждение компилятора (уровень 1) C4020
ms.date: 11/04/2016
f1_keywords:
- C4020
helpviewer_keywords:
- C4020
ms.assetid: 8c4cd6be-9371-4c8c-b0ff-a5ad367bbab0
ms.openlocfilehash: 454bab1eb8a3d1da6d0fe8bf508de8c466d22001
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97241577"
---
# <a name="compiler-warning-level-1-c4020"></a>Предупреждение компилятора (уровень 1) C4020

"функция": слишком много фактических параметров

Число фактических параметров в вызове функции превышает число формальных параметров в прототипе или определении функции. Компилятор передает дополнительные фактические параметры в соответствии с соглашением о вызовах функции.

Следующий пример приводит к возникновению ошибки C4020:

```c
// C4020.c
// compile with: /W1 /c
void f(int);
int main() {
   f(1,2);   // C4020
}
```

Возможное решение:

```c
// C4020b.c
// compile with: /c
void f(int);
int main() {
   f(1);
}
```
