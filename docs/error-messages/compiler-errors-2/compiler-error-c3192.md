---
description: 'Дополнительные сведения о: Ошибка компилятора C3192'
title: Ошибка компилятора C3192
ms.date: 11/04/2016
f1_keywords:
- C3192
helpviewer_keywords:
- C3192
ms.assetid: 8b0083d4-706f-46f6-858a-e1d9af464cf8
ms.openlocfilehash: fc88480a7ef799ced07dc52491b394b432e6525e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97241915"
---
# <a name="compiler-error-c3192"></a>Ошибка компилятора C3192

Синтаксическая ошибка: "^" не является префиксным оператором (возможно, имелось в виду "*"?)

В качестве оператора разыменования нельзя использовать маркер.

Следующий пример приводит к возникновению ошибки C3192:

```cpp
// C3192.cpp
// compile with: /clr
using namespace System;

ref class MyClass {
public:
   MyClass () {}
   MyClass(MyClass%) {}
};

int main() {
   MyClass ^ s = gcnew MyClass;
   MyClass b = ^s;   // C3192

   // OK
   MyClass b2 = *s;
}
```
