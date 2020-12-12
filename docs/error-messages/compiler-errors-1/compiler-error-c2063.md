---
description: 'Дополнительные сведения о: Ошибка компилятора C2063'
title: Ошибка компилятора C2063
ms.date: 11/04/2016
f1_keywords:
- C2063
helpviewer_keywords:
- C2063
ms.assetid: 0a90c18f-4029-416a-9128-e8713b53e6f1
ms.openlocfilehash: 18b2cd6bf68144245b85d744923404f4a27d63f0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97328618"
---
# <a name="compiler-error-c2063"></a>Ошибка компилятора C2063

"идентификатор": не является функцией

Идентификатор используется в качестве функции, но не объявлен как функция.

Следующий пример приводит к возникновению ошибки C2063:

```c
// C2063.c
int main() {
   int i, j;
   j = i();    // C2063, i is not a function
}
```

Возможное решение:

```c
// C2063b.c
int i() { return 0;}
int main() {
   int j;
   j = i();
}
```
