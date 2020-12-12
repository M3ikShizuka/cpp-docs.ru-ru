---
description: 'Дополнительные сведения о: Ошибка компилятора c2050'
title: Ошибка компилятора c2050
ms.date: 11/04/2016
f1_keywords:
- C2050
helpviewer_keywords:
- C2050
ms.assetid: 66aaed7d-00db-4ce1-a9d6-4447c1cf07ce
ms.openlocfilehash: a6e6221b0985ee509953b517ae04de9f0962fe3a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97175044"
---
# <a name="compiler-error-c2050"></a>Ошибка компилятора c2050

выражение switch не является целым

**`switch`** Результатом вычисления выражения является нецелочисленное значение. Чтобы устранить эту ошибку, используйте только целочисленные значения в операторах switch.

Следующий пример приводит к возникновению ошибки c2050:

```cpp
// C2050.cpp
int main() {
   int a = 1;
   switch ("a") {   // C2050
      case 1:
         a = 0;
      default:
         a = 2;
   }
}
```

Возможное решение:

```cpp
// C2050b.cpp
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
