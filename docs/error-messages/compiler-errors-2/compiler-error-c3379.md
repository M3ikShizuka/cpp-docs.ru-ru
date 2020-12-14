---
description: 'Дополнительные сведения о: Ошибка компилятора C3379'
title: Ошибка компилятора C3379
ms.date: 11/04/2016
f1_keywords:
- C3379
helpviewer_keywords:
- C3379
ms.assetid: a66c2c4e-091c-4426-9cde-7c4cfb2ffce1
ms.openlocfilehash: 622a1327eb84d83fa24d8a084e3266183c669120
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97220738"
---
# <a name="compiler-error-c3379"></a>Ошибка компилятора C3379

"класс": вложенный класс не может иметь спецификатор доступа к сборке в рамках своего объявления

При применении к управляемому типу, например классу или структуре, ключевые слова [Public](../../cpp/public-cpp.md) и [Private](../../cpp/private-cpp.md) указывают, будет ли класс предоставлен через метаданные сборки. `public` или `private` нельзя применить к вложенному классу, который будет наследовать доступ к сборке включающего класса.

При использовании с [/CLR](../../build/reference/clr-common-language-runtime-compilation.md) `ref` `value` Ключевые слова и указывают на то, что класс является управляемым (см. раздел [классы и структуры](../../extensions/classes-and-structs-cpp-component-extensions.md)).

Следующий пример приводит к возникновению ошибки C3379:

```cpp
// C3379a.cpp
// compile with: /clr
using namespace System;

public ref class A {
public:
   static int i = 9;

   public ref class BA {   // C3379
   // try the following line instead
   // ref class BA {
   public:
      static int ii = 8;
   };
};

int main() {

   A^ myA = gcnew A;
   Console::WriteLine(myA->i);

   A::BA^ myBA = gcnew A::BA;
   Console::WriteLine(myBA->ii);
}
```
