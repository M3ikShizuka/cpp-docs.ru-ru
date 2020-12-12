---
description: 'Дополнительные сведения о: Ошибка компилятора C2140'
title: Ошибка компилятора C2140
ms.date: 11/04/2016
f1_keywords:
- C2140
helpviewer_keywords:
- C2140
ms.assetid: d44a0500-002c-4632-9e5e-c71c3a473ec4
ms.openlocfilehash: b9292019ce9a17c8f1dabca87f61f27b21494a82
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97124154"
---
# <a name="compiler-error-c2140"></a>Ошибка компилятора C2140

"тип": тип, зависящий от параметра универсального типа, не допускается в качестве аргумента для встроенной характеристики типа "характеристика" компилятора

В характеристике типа передан недопустимый спецификатор типа.

Дополнительные сведения см. в статье [Compiler Support for Type Traits (C++/CLI and C++/CX)](../../extensions/compiler-support-for-type-traits-cpp-component-extensions.md) (Поддержка характеристик типов компилятором (C++/CLI and C++/CX)).

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C2140.

```cpp
// C2140.cpp
// compile with: /clr /c
template <class T>

struct is_polymorphic {
   static const bool value = __is_polymorphic(T);
};

class x {};

generic <class T>
ref class C {
   void f() {
      System::Console::WriteLine(__is_polymorphic(T));   // C2140
      System::Console::WriteLine(is_polymorphic<T>::value);   // C2140

      System::Console::WriteLine(__is_polymorphic(x));   // OK
      System::Console::WriteLine(is_polymorphic<x>::value);   // OK
   }
};
```
