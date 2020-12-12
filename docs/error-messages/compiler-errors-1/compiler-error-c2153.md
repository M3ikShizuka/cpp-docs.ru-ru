---
description: 'Дополнительные сведения о: Ошибка компилятора C2153'
title: Ошибка компилятора C2153
ms.date: 11/04/2016
f1_keywords:
- C2153
helpviewer_keywords:
- C2153
ms.assetid: cfc50cb7-9a0f-4b5b-879a-d419c99f7be1
ms.openlocfilehash: 0b5ded0908f3c12033f1c2b3b034b41b52e847cb
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97181297"
---
# <a name="compiler-error-c2153"></a>Ошибка компилятора C2153

шестнадцатеричные константы должны содержать по крайней мере одну шестнадцатеричную цифру

Шестнадцатеричные константы 0x, 0X и \x недопустимы. По крайней мере одна шестнадцатеричная цифра должна следовать за x или X.

Следующий пример приводит к возникновению ошибки C2153:

```cpp
// C2153.cpp
int main() {
   int a= 0x;    // C2153
   int b= 0xA;   // OK
}
```
