---
description: 'Дополнительные сведения о: Ошибка компилятора C2739'
title: Ошибка компилятора C2739
ms.date: 11/04/2016
f1_keywords:
- C2739
helpviewer_keywords:
- C2739
ms.assetid: 5b63e435-7631-43d7-805e-f2adefb7e517
ms.openlocfilehash: 2a65f552eeb8a0b475b5559aaa3f1ab6b0da0e25
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97123088"
---
# <a name="compiler-error-c2739"></a>Ошибка компилятора C2739

number: явно задаваемый управляемый массив или массив WinRT может иметь размерность от 1 до 32

Измерение массива не входило в диапазон от 1 до 32.

В следующем примере показано возникновение ошибки C2739 и приводятся сведения по ее устранению.

```cpp
// C2739.cpp
// compile with: /clr
int main() {
   array<int, -1>^a;   // C2739
   // try the following line instead
   // array<int, 2>^a;
}
```
