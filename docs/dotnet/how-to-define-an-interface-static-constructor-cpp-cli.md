---
description: Дополнительные сведения см. в статье как определить статический конструктор интерфейса (C++/CLI)
title: Практическое руководство. Определение статического конструктора интерфейса (C++/CLI)
ms.date: 11/04/2016
helpviewer_keywords:
- constructors [C++]
- static constructors, interface
- interface static constructor
ms.assetid: 1f031cb2-e94f-43dc-819b-44cf2faaaa49
ms.openlocfilehash: 2cc6eca19a26f9857c029fc01c500ed9f4691e8d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97245906"
---
# <a name="how-to-define-an-interface-static-constructor-ccli"></a>Практическое руководство. Определение статического конструктора интерфейса (C++/CLI)

Интерфейс может иметь статический конструктор, который можно использовать для инициализации статических элементов данных.  Статический конструктор будет вызываться только один раз и будет вызываться до первого обращения к статическому члену интерфейса.

## <a name="example"></a>Пример

```cpp
// mcppv2_interface_class2.cpp
// compile with: /clr
using namespace System;

interface struct MyInterface {
   static int i;
   static void Test() {
      Console::WriteLine(i);
   }

   static MyInterface() {
      Console::WriteLine("in MyInterface static constructor");
      i = 99;
   }
};

ref class MyClass : public MyInterface {};

int main() {
   MyInterface::Test();
   MyClass::MyInterface::Test();

   MyInterface ^ mi = gcnew MyClass;
   mi->Test();
}
```

```Output
in MyInterface static constructor
99
99
99
```

## <a name="see-also"></a>См. также раздел

[Класс interface](../extensions/interface-class-cpp-component-extensions.md)
