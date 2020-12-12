---
description: 'Дополнительные сведения о: Ошибка компилятора C3653'
title: Ошибка компилятора C3653
ms.date: 11/04/2016
f1_keywords:
- C3653
helpviewer_keywords:
- C3653
ms.assetid: 316549d7-f7ef-4578-a2ba-57adc8aac527
ms.openlocfilehash: 6f41d52416d2fee05873197efa60e4b888cf29f1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97320109"
---
# <a name="compiler-error-c3653"></a>Ошибка компилятора C3653

"функция": не может использоваться в качестве именованного переопределения: переопределяемая функция не найдена; забыли явно задать имя функции с помощью оператора::?

Явное переопределение указывает функцию, которая не была найдена ни в одном интерфейсе. Дополнительные сведения см. в разделе [явные переопределения](../../extensions/explicit-overrides-cpp-component-extensions.md).

Следующий пример приводит к возникновению ошибки C3653:

```cpp
// C3653.cpp
// compile with: /clr
public interface struct I {
   void h();
};

public ref struct X : public I {
   virtual void f() new sealed = J {};   // C3653 no J in scope
   virtual void g() {}   // OK
   virtual void h() new sealed = I::h {};   // OK
};
```
