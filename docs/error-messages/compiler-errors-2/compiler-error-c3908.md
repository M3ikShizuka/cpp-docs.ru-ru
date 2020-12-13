---
description: 'Дополнительные сведения о: Ошибка компилятора C3908'
title: Ошибка компилятора C3908
ms.date: 11/04/2016
f1_keywords:
- C3908
helpviewer_keywords:
- C3908
ms.assetid: 3c322482-c79e-4197-a578-2ad9bc379d1a
ms.openlocfilehash: 67258f9f5946d180af9a270b931f88f263238856
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97144174"
---
# <a name="compiler-error-c3908"></a>Ошибка компилятора C3908

уровень доступа менее четкий, чем "конструкция"

Метод доступа к свойству (Get или Set) не может иметь менее четкий доступ, чем указанный в самом свойстве.  Аналогичным образом для методов доступа к событиям.

Дополнительные сведения см. в разделе [свойство](../../extensions/property-cpp-component-extensions.md) и [событие](../../extensions/event-cpp-component-extensions.md).

Следующий пример приводит к возникновению ошибки C3908:

```cpp
// C3908.cpp
// compile with: /clr
ref class X {
protected:
   property int i {
   public:   // C3908 property i is protected
      int get();
   private:
      void set(int);   // OK more restrictive
   };
};
```
