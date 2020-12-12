---
description: 'Дополнительные сведения о: Ошибка компилятора C2048'
title: Ошибка компилятора C2048
ms.date: 11/04/2016
f1_keywords:
- C2048
helpviewer_keywords:
- C2048
ms.assetid: 44704726-85fc-42f0-afb9-194df8c4ca7c
ms.openlocfilehash: cc87d0ca1670daa4cb137f4c3053030d188884e4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97175083"
---
# <a name="compiler-error-c2048"></a>Ошибка компилятора C2048

несколько вариантов, используемых по умолчанию

**`switch`** Оператор содержит несколько **`default`** меток. Удалите одну из **`default`** меток, чтобы устранить эту ошибку.

В следующем примере возникает ошибка C2048:

```cpp
// C2048.cpp
int main() {
   int a = 1;
   switch (a) {
      case 1:
         a = 0;
      default:
         a = 2;
      default:   // C2048
         a = 3;
   }
}
```

Возможное решение:

```cpp
// C2048b.cpp
int main() {
   int a = 1;
   switch (a) {
      case 1:
         a = 0;
      default:
         a = 2;
   }
}
```
