---
description: 'Дополнительные сведения о: Ошибка компилятора C2247'
title: Ошибка компилятора C2247
ms.date: 11/04/2016
f1_keywords:
- C2247
helpviewer_keywords:
- C2247
ms.assetid: 72efa03e-615e-4ef9-aede-0a98654b20fd
ms.openlocfilehash: 480d3862a1f96517ecce11be5c695e106eb58d7e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97177943"
---
# <a name="compiler-error-c2247"></a>Ошибка компилятора C2247

"идентификатор" недоступен, так как "класс" использует "спецификатор" для наследования от "class"

`identifier` наследуется от класса, объявленного с закрытым или защищенным доступом.

Следующий пример приводит к возникновению ошибки C2247:

```cpp
// C2247.cpp
class A {
public:
   int i;
};
class B : private A {};    // B inherits a private A
class C : public B {} c;   // so even though C's B is public
int j = c.i;               // C2247, i not accessible
```

Эта ошибка также может быть вызвана работой по согласованности компилятора, выполненной для Visual Studio .NET 2003: контроль доступа с защищенными членами. Доступ к защищенному члену (n) возможен только через функцию-член класса (B), который наследует от класса (A), членом которого он является (n).

Для кода, который допустим в версиях Visual Studio .NET 2003 и Visual Studio .NET Visual C++, объявите элемент дружественным по отношению к типу. Также можно использовать открытое наследование.

```cpp
// C2247b.cpp
// compile with: /c
// C2247 expected
class A {
public:
   void f();
   int n;
};

class B: protected A {
   // Uncomment the following line to resolve.
   // friend void A::f();
};

void A::f() {
   B b;
   b.n;
}
```

C2247 также можно создать в результате действий по согласованности компилятора, выполненных для Visual Studio .NET 2003: закрытые базовые классы теперь недоступны. Класс (A), являющийся закрытым базовым классом для типа (B), не должен быть доступен для типа (C), в котором в качестве базового класса используется B.

Для кода, который допустим в версиях Visual Studio .NET 2003 и Visual Studio .NET Visual C++, используйте оператор SCOPE.

```cpp
// C2247c.cpp
// compile with: /c
struct A {};

struct B: private A {};

struct C : B {
   void f() {
      A *p1 = (A*) this;   // C2247
      // try the following line instead
      // ::A *p2 = (::A*) this;
   }
};
```
