---
description: 'Дополнительные сведения о: Ошибка компилятора C3910'
title: Ошибка компилятора C3910
ms.date: 11/04/2016
f1_keywords:
- C3910
helpviewer_keywords:
- C3910
ms.assetid: cfcbe620-b463-463b-95ea-2d60ad33ebb5
ms.openlocfilehash: 802aac0d27e230920a906b96afc78100296c75de
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97144148"
---
# <a name="compiler-error-c3910"></a>Ошибка компилятора C3910

"событие": необходимо определить член "метод"

Событие было определено, но не содержит указанный, необходимый метод доступа.

Дополнительные сведения см. в разделе [event](../../extensions/event-cpp-component-extensions.md).

Следующий пример приводит к возникновению ошибки C3910:

```cpp
// C3910.cpp
// compile with: /clr /c
delegate void H();
ref class X {
   event H^ E {
      // uncomment the following lines
      // void add(H^) {}
      // void remove( H^ h ) {}
      // void raise( ) {}
   };   // C3910

   event H^ E2; // OK data member
};
```
