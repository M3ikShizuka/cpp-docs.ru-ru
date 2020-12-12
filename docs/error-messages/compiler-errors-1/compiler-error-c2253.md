---
description: 'Дополнительные сведения о: Ошибка компилятора C2253'
title: Ошибка компилятора C2253
ms.date: 11/04/2016
f1_keywords:
- C2253
helpviewer_keywords:
- C2253
ms.assetid: bd6445ae-b2c1-4669-9657-a8f4acf80b16
ms.openlocfilehash: 7401e9a25382f635ec076e9d84b02e58935bbddd
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97134788"
---
# <a name="compiler-error-c2253"></a>Ошибка компилятора C2253

"функция": чистый спецификатор или абстрактный спецификатор переопределения допускаются только для виртуальной функции

Невиртуальная функция указана как чистая **`virtual`** .

Следующий пример приводит к возникновению ошибки C2253:

```cpp
// C2253.cpp
// compile with: /c
class A {
public:
   void func1() = 0;   // C2253 not virtual
   virtual void func2() = 0;   // OK
};
```

Следующий пример приводит к возникновению ошибки C2253:

```cpp
// C2253_2.cpp
// compile with: /clr /c
ref struct A {
   property int Prop_3 {
      int get() abstract;   // C2253
      // try the following line instead
      // virtual int get() abstract;

      void set(int i) abstract;   // C2253
      // try the following line instead
      // virtual void set(int i) abstract;
   }
};
```
