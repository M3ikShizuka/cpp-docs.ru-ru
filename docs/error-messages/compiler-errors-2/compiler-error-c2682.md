---
description: 'Дополнительные сведения о: Ошибка компилятора C2682'
title: Ошибка компилятора C2682
ms.date: 11/04/2016
f1_keywords:
- C2682
helpviewer_keywords:
- C2682
ms.assetid: 30c6a7c4-f5f7-4fe8-81a8-c48938521ab4
ms.openlocfilehash: 962debb0227347abe97e290db724fdb227212914
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97177436"
---
# <a name="compiler-error-c2682"></a>Ошибка компилятора C2682

невозможно использовать casting_operator для преобразования из "тип1" в "тип2"

Оператор приведения попытался выполнить преобразование между несовместимыми типами. Например, оператор [dynamic_cast](../../cpp/dynamic-cast-operator.md) нельзя использовать для преобразования указателя в ссылку. **`dynamic_cast`** Оператор не может использоваться для приведения квалификаторов. Все квалификаторы типов должны совпадать.

Оператор можно использовать **`const_cast`** для удаления таких атрибутов **`const`** , как, **`volatile`** или **`__unaligned`** .

Следующий пример приводит к возникновению ошибки C2682:

```cpp
// C2682.cpp
class A { virtual void f(); };
class B: public A {};

void g(A* pa) {
    B& rb = dynamic_cast<B&>(pa); // C2682
}
```

Следующий пример приводит к возникновению ошибки C2682:

```cpp
// C2682b.cpp
// compile with: /clr
ref struct R{};
ref struct RR : public R{};
ref struct H {
   RR^ r ;
   short s;
   int i;
};

int main() {
   H^ h = gcnew H();
   interior_ptr<int>lr = &(h->i);
   interior_ptr<short>ssr = safe_cast<interior_ptr<short> >(lr);   // C2682
   interior_ptr<short>ssr = reinterpret_cast<interior_ptr<short> >(lr);   // OK
}
```
