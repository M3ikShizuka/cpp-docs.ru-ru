---
description: 'Дополнительные сведения о: Ошибка компилятора C2250'
title: Ошибка компилятора C2250
ms.date: 11/04/2016
f1_keywords:
- C2250
helpviewer_keywords:
- C2250
ms.assetid: f990986f-5c7d-4af4-a25c-b35540f1e217
ms.openlocfilehash: 5d018a01899ac74f148b2f0467feff9d7cecc025
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97134845"
---
# <a name="compiler-error-c2250"></a>Ошибка компилятора C2250

"идентификатор": неоднозначное наследование "класс:: член"

Производный класс наследует больше одного переопределения виртуальной функции виртуального базового класса. Эти переопределения являются неоднозначными в производном классе.

При компиляции следующего примера возникнет ошибка C2286:

```cpp
// C2250.cpp
// compile with: /c
// C2250 expected
struct V {
   virtual void vf();
};

struct A : virtual V {
   void vf();
};

struct B : virtual V {
   void vf();
};

struct D : A, B {
   // Uncomment the following line to resolve.
   // void vf();
};
```
