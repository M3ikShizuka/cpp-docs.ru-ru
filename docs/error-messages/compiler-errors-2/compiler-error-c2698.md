---
description: 'Дополнительные сведения о: Ошибка компилятора C2698'
title: Ошибка компилятора C2698
ms.date: 11/04/2016
f1_keywords:
- C2698
helpviewer_keywords:
- C2698
ms.assetid: 3ebfe395-c20b-4c56-9980-ca9ed8653382
ms.openlocfilehash: a787c43e7a885734f4c6a2d76aa16d51e19615c5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97326634"
---
# <a name="compiler-error-c2698"></a>Ошибка компилятора C2698

объявление using для "объявление 1" не может существовать вместе с существующим объявлением using для "объявление 2"

После [объявления using](../../cpp/using-declaration.md) для элемента данных любое объявление using в той же области, которое использует такое же имя, не разрешается, так как только функции могут быть перегружены.

Следующий пример приводит к возникновению ошибки C2698:

```cpp
// C2698.cpp
struct A {
   int x;
};

struct B {
   int x;
};

struct C : A, B {
   using A::x;
   using B::x;   // C2698
}
```
