---
description: 'Дополнительные сведения о: Ошибка компилятора C2139'
title: Ошибка компилятора C2139
ms.date: 11/04/2016
f1_keywords:
- C2139
helpviewer_keywords:
- C2139
ms.assetid: 31e047c0-5bf9-46c2-b6de-b627ea6a5768
ms.openlocfilehash: 240d1cdd4144e77a31063985a8a1fffb6992196c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97323068"
---
# <a name="compiler-error-c2139"></a>Ошибка компилятора C2139

"тип": неопределенный класс не может использоваться в качестве аргумента для встроенного типа "характеристика" компилятора

Признаку типа передан недопустимый аргумент.

Дополнительные сведения см. в статье [Compiler Support for Type Traits (C++/CLI and C++/CX)](../../extensions/compiler-support-for-type-traits-cpp-component-extensions.md) (Поддержка характеристик типов компилятором (C++/CLI and C++/CX)).

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C2139.

```cpp
// C2139.cpp
// compile with: /EHsc
#include <iostream>
using namespace std;

template <class T>
struct is_polymorphic {
   static const bool value = __is_polymorphic(T);
};

class C;
class D {};

class E {
public:
   virtual void Test() {}
};

int main() {
   cout << is_polymorphic<C>::value << endl;   // C2139
   cout << is_polymorphic<D>::value << endl;   // OK
   cout << is_polymorphic<E>::value << endl;   // OK
}
```
