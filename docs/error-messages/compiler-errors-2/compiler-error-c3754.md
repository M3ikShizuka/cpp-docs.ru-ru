---
description: 'Дополнительные сведения о: Ошибка компилятора C3754'
title: Ошибка компилятора C3754
ms.date: 11/04/2016
f1_keywords:
- C3754
helpviewer_keywords:
- C3754
ms.assetid: 14b877bc-9277-40ec-af1c-196a58b45f10
ms.openlocfilehash: 1f6c32a94caf6b2045f177480f76aa0c7fc2a7fd
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97340142"
---
# <a name="compiler-error-c3754"></a>Ошибка компилятора C3754

конструктор делегата: функцию члена "Function" нельзя вызывать для экземпляра типа "тип"

Выполнен вызов функции с помощью указателя на тип, который не содержит функцию.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3754:

```cpp
// C3754a.cpp
// compile with: /clr
using namespace System;

delegate void MyDel();

interface class MyInterface {};

ref struct MyClass : MyInterface {
   void f() {}
};

int main() {
   MyInterface^ p = gcnew MyClass;
   MyDel^ q = gcnew MyDel(p, &MyClass::f);   // C3754
   // try the following line instead
//   MyDel^ q = gcnew MyDel(safe_cast<MyClass^>(p), &MyClass::f);
}
```
