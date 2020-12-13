---
description: 'Дополнительные сведения о: Ошибка компилятора C2255'
title: Ошибка компилятора C2255
ms.date: 11/04/2016
f1_keywords:
- C2255
helpviewer_keywords:
- C2255
ms.assetid: 67dc4cb0-de6b-4405-bd64-d47736367a93
ms.openlocfilehash: 9c7898ede43c9c25175854faeab5ee279a9c5635
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97333860"
---
# <a name="compiler-error-c2255"></a>Ошибка компилятора C2255

"элемент": не допускается вне определения класса

Например, функция, не являющийся членом, объявляется **`friend`** .

При компиляции следующего примера возникнет ошибка C2255:

```cpp
// C2255.cpp
// compile with: /c
class A {
private:
   void func1();
   friend void func2();
};

friend void func1() {}   // C2255
void func2(){}
```
