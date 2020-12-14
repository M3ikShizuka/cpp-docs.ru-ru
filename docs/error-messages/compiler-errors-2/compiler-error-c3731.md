---
description: 'Дополнительные сведения о: Ошибка компилятора C3731'
title: Ошибка компилятора C3731
ms.date: 11/04/2016
f1_keywords:
- C3731
helpviewer_keywords:
- C3731
ms.assetid: 45f89fcd-464c-4bc8-8a42-edcb5416d26c
ms.openlocfilehash: 8a7ad836083a8c103df7becd7605a0dfd0efeea7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97245087"
---
# <a name="compiler-error-c3731"></a>Ошибка компилятора C3731

несовместимое событие "функция1" и обработчик "функция2"; Источник события и обработчик событий должны быть одного типа

Источник события и получатель события должны иметь одинаковый тип (например, `native` и `com` типы). Чтобы устранить эту ошибку, сделайте так, чтобы типы источника события и обработчика событий совпадали.

Следующий пример приводит к возникновению ошибки C3731:

```cpp
// C3731.cpp
// compile with: /clr
#using <mscorlib.dll>
[event_source(native)]
struct A {
   __event void MyEvent();
};

[event_receiver(managed)]
// try the following line instead
// [event_receiver(native)]
struct B {
   void func();
   B(A a) {
      __hook(&A::MyEvent, &a, &B::func);   // C3731
   }
};

int main() {
}
```
