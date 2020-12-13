---
description: 'Дополнительные сведения о: Ошибка компилятора C2553'
title: Ошибка компилятора C2553
ms.date: 11/04/2016
f1_keywords:
- C2553
helpviewer_keywords:
- C2553
ms.assetid: 64bc1e9a-627f-4ce9-b7bc-dc911bdb9180
ms.openlocfilehash: 5f5e3eb9d94935aa8e6974f72517e7193ba07db3
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97134502"
---
# <a name="compiler-error-c2553"></a>Ошибка компилятора C2553

"base_function": возвращаемый тип переопределяемой виртуальной функции отличается от "override_function"

Функция в производном классе попыталась переопределить виртуальную функцию в базовом классе, но функция производного класса не имеет того же типа возвращаемого значения, что и функция базового класса.  Сигнатура функции переопределения должна соответствовать сигнатуре переопределяемой функции.

Следующий пример приводит к возникновению ошибки C2553:

```cpp
// C2553.cpp
// compile with: /clr /c
ref struct C {
   virtual void f();
};

ref struct D : C {
   virtual int f() override ;   // C2553

   // try the following line instead
   // virtual void f() override;
};
```
