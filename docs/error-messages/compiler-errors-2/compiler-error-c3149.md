---
description: 'Дополнительные сведения о: Ошибка компилятора C3149'
title: Ошибка компилятора C3149
ms.date: 11/04/2016
f1_keywords:
- C3149
helpviewer_keywords:
- C3149
ms.assetid: cf6e2616-2f06-46da-8a8a-d449cb481c51
ms.openlocfilehash: 596a8d2728e7598a737da4aa5a1650df669db969
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97322094"
---
# <a name="compiler-error-c3149"></a>Ошибка компилятора C3149

"тип": невозможно использовать этот тип здесь без "char" верхнего уровня

Объявление указано неправильно.

Например, вы могли определить тип CLR в глобальной области и попытаться создать переменную типа как часть определения. Так как глобальные переменные типов CLR не допускаются, компилятор создаст C3149.

Чтобы устранить эту ошибку, объявите переменные типов CLR в определении функции или типа.

Следующий пример приводит к возникновению ошибки C3149:

```cpp
// C3149.cpp
// compile with: /clr
using namespace System;
int main() {
   // declare an array of value types
   array< Int32 ^> IntArray;   // C3149
   array< Int32>^ IntArray2;   // OK
}
```

Следующий пример приводит к возникновению ошибки C3149:

```cpp
// C3149b.cpp
// compile with: /clr /c
delegate int MyDelegate(const int, int);
void Test1(MyDelegate m) {}   // C3149
void Test2(MyDelegate ^ m) {}   // OK
```
