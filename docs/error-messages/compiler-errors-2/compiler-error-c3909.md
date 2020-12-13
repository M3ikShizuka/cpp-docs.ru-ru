---
description: 'Дополнительные сведения о: Ошибка компилятора C3909'
title: Ошибка компилятора C3909
ms.date: 11/04/2016
f1_keywords:
- C3909
helpviewer_keywords:
- C3909
ms.assetid: 0a443132-e53f-42dc-a58b-f086da3e7bfd
ms.openlocfilehash: a85e0201e192caae1e4f170a12544177cbb2d7f9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97144161"
---
# <a name="compiler-error-c3909"></a>Ошибка компилятора C3909

Авинрт или объявление управляемого события должно выполняться в WinRT или управляемом типе

Событие среды выполнения Windows или управляемое событие было объявлено в собственном типе. Чтобы устранить эту ошибку, объявите события в типах среды выполнения Windows или управляемых типах.

Дополнительные сведения см. в разделе [event](../../extensions/event-cpp-component-extensions.md).

В следующем примере показано возникновение ошибки C3909 и приводятся сведения по ее устранению.

```cpp
// C3909.cpp
// compile with: /clr /c
delegate void H();
class X {
   event H^ E;   // C3909 - use ref class X instead
};

ref class Y {
   static event H^ E {
      void add(H^) {}
      void remove( H^ h ) {}
      void raise( ) {}
   }
};
```
