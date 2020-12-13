---
description: 'Дополнительные сведения о: Ошибка компилятора C3642'
title: Ошибка компилятора C3642
ms.date: 11/04/2016
f1_keywords:
- C3642
helpviewer_keywords:
- C3642
ms.assetid: 429790c2-9614-4d85-b31c-687c8d8f83ff
ms.openlocfilehash: 77d65d2bb2c426fe78671328b0eccab739b9dabe
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97340311"
---
# <a name="compiler-error-c3642"></a>Ошибка компилятора C3642

"return_type/args": невозможно вызвать функцию с __clrcallным соглашением о вызовах из машинного кода

Функция, помеченная соглашением о вызовах [__clrcall](../../cpp/clrcall.md) , не может быть вызвана из машинного (неуправляемого) кода.

*return_type/args* — это либо имя функции, либо тип `__clrcall` функции, которую вы пытаетесь вызвать.  Тип используется при вызове через указатель на функцию.

Чтобы вызвать управляемую функцию из собственного контекста, можно добавить функцию-оболочку, которая будет вызывать `__clrcall` функцию. Также можно использовать механизм маршалирования среды CLR. Дополнительные сведения см. [в разделе инструкции. маршалирование указателей функций с помощью PInvoke](../../dotnet/how-to-marshal-function-pointers-using-pinvoke.md) .

Следующий пример приводит к возникновению ошибки C3642:

```cpp
// C3642.cpp
// compile with: /clr
using namespace System;
struct S {
   void Test(String ^ s) {   // CLR type in signature, implicitly __clrcall
      Console::WriteLine(s);
   }
   void Test2(char * s) {
      Test(gcnew String(s));
   }
};

#pragma unmanaged
int main() {
   S s;
   s.Test("abc");   // C3642
   s.Test2("abc");   // OK
}
```
