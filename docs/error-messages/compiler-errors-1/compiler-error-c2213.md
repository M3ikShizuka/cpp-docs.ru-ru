---
description: 'Дополнительные сведения о: Ошибка компилятора C2213'
title: Ошибка компилятора C2213
ms.date: 11/04/2016
f1_keywords:
- C2213
helpviewer_keywords:
- C2213
ms.assetid: ff012278-7f3b-4d49-aaed-2349756f6225
ms.openlocfilehash: aa9274f77c2416af286c306f2e6302b5f416a24b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97245594"
---
# <a name="compiler-error-c2213"></a>Ошибка компилятора C2213

"модификатор": недопустимый аргумент для __based

Изменение аргумента **`__based`** недопустимо.

Следующий пример приводит к возникновению ошибки C2213:

```cpp
// C2213.cpp
// compile with: /c
int i;
int *j;
char __based(i) *p;   // C2213
char __based(j) *p2;   // OK
```
