---
description: 'Дополнительные сведения о: Ошибка компилятора C3374'
title: Ошибка компилятора C3374
ms.date: 11/04/2016
f1_keywords:
- C3374
helpviewer_keywords:
- C3374
ms.assetid: 41431299-bd20-47d4-a0c8-1334dd79018b
ms.openlocfilehash: b3ec1a18433c41f8c1e1a4b704b6ab03dae7572d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97245178"
---
# <a name="compiler-error-c3374"></a>Ошибка компилятора C3374

невозможно взять адрес 'функции' без создания экземпляра делегата

Адрес функции был взят в контексте, отличном от создания экземпляра делегата.

Следующий пример приводит к возникновению ошибки C3374:

```cpp
// C3374.cpp
// compile with: /clr
public delegate void MyDel(int i);

ref class A {
public:
   void func1(int i) {
      System::Console::WriteLine("in func1 {0}", i);
   }
};

int main() {
   &A::func1;   // C3374

   // OK
   A ^ a = gcnew A;
   MyDel ^ StaticDelInst = gcnew MyDel(a, &A::func1);
}
```

## <a name="see-also"></a>См. также раздел

[Практическое руководство. Определение и использование делегатов (C++/CLI)](../../dotnet/how-to-define-and-use-delegates-cpp-cli.md)
