---
description: 'Дополнительные сведения о: Ошибка компилятора C3900'
title: Ошибка компилятора C3900
ms.date: 11/04/2016
f1_keywords:
- C3900
helpviewer_keywords:
- C3900
ms.assetid: a94cc561-8fa8-4344-9e01-e81ff462fae5
ms.openlocfilehash: 7b210eb6369b8953f36821d45690de8656113af2
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97238938"
---
# <a name="compiler-error-c3900"></a>Ошибка компилятора C3900

"член": не допускается в текущей области

Блоки свойств могут содержать только объявления функций и встроенные определения функций. В блоках свойств не допускаются никакие члены, кроме функций. Не допускаются определения типов, операторы и дружественные функции. Для получения дополнительной информации см. [property](../../extensions/property-cpp-component-extensions.md).

Определения событий могут содержать только методы доступа и функции.

Следующий пример приводит к возникновению ошибки C3900:

```cpp
// C3900.cpp
// compile with: /clr
ref class X {
   property int P {
      void set(int);   // OK
      int i;   // C3900 variable declaration
   };
};
```

Следующий пример приводит к возникновению ошибки C3900:

```cpp
// C3900b.cpp
// compile with: /clr
using namespace System;
delegate void H();
ref class X {
   event H^ E {
      int m;   // C3900

      // OK
      void Test() {}

      void add( H^ h ) {}
      void remove( H^ h ) {}
      void raise( ) {}
   }
};
```
