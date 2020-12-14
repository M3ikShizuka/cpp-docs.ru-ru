---
description: 'Дополнительные сведения о: Ошибка компилятора C3185'
title: Ошибка компилятора C3185
ms.date: 11/04/2016
f1_keywords:
- C3185
helpviewer_keywords:
- C3185
ms.assetid: 5bf96279-043c-4981-9d02-b4550071b192
ms.openlocfilehash: 7dbcf11aa7c88d883aeccc8325832849f8b7a238
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97242019"
---
# <a name="compiler-error-c3185"></a>Ошибка компилятора C3185

typeid используется для управляемого типа или типа WinRT "type", вместо этого используйте operator

Нельзя применить оператор [typeid](../../cpp/typeid-operator.md) к типу управляемого или WinRT. Вместо этого используйте [typeid](../../extensions/typeid-cpp-component-extensions.md) .

В следующем примере показано возникновение ошибки C3185 и приводятся сведения по ее устранению.

```cpp
// C3185a.cpp
// compile with: /clr
ref class Base {};
ref class Derived : public Base {};

int main() {
   Derived ^ pd = gcnew Derived;
   Base ^pb = pd;
   const type_info & t1 = typeid(pb);   // C3185
   System::Type ^ MyType = Base::typeid;   // OK
};
```
