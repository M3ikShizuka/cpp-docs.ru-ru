---
description: 'Дополнительные сведения о: Ошибка компилятора C2748'
title: Ошибка компилятора C2748
ms.date: 11/04/2016
f1_keywords:
- C2748
helpviewer_keywords:
- C2748
ms.assetid: b63ac78b-a200-499c-afea-15af1a1e819e
ms.openlocfilehash: 64720391906777ffd5f36c53e6f7ce27940426fd
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97123023"
---
# <a name="compiler-error-c2748"></a>Ошибка компилятора C2748

при создании управляемого массива или массива WinRT следует указать размер массива или инициализатор массива

Неправильный формат управляемого массива или массива WinRT. Дополнительные сведения см. в описании [array](../../extensions/arrays-cpp-component-extensions.md).

В следующем примере показано возникновение ошибки C2748 и приводятся сведения по ее устранению.

```cpp
// C2748.cpp
// compile with: /clr
int main() {
   array<int> ^p1 = new array<int>();   // C2748
   // try the following line instead
   array<int> ^p2 = new array<int>(2);
}
```
