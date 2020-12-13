---
description: 'Дополнительные сведения о: Ошибка компилятора C2688'
title: Ошибка компилятора C2688
ms.date: 11/04/2016
f1_keywords:
- C2688
helpviewer_keywords:
- C2688
ms.assetid: 168c9e9d-8f65-4664-af86-db71d3e6ee46
ms.openlocfilehash: 17219fe6f4358b73ace0435e60d8fc2b7a9b6df8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97330679"
---
# <a name="compiler-error-c2688"></a>Ошибка компилятора C2688

"C2:: ФГрВ": ковариантные возвраты с несколькими или виртуальными наследованиями не поддерживаются для функций varargs

Ковариантные возвращаемые типы не поддерживаются в Visual C++, если функция содержит переменные аргументы.

Чтобы устранить эту ошибку, определите функции, чтобы они не использовали переменные аргументы, или сделайте возвращаемые значения одинаковыми для всех виртуальных функций.

Следующий пример приводит к возникновению ошибки C2688:

```cpp
// C2688.cpp
struct G1 {};
struct G2 {};
struct G3 : G1, G2 {};
struct G4 {};
struct G5 {};
struct G6 : G4, G5 {};
struct G7 : G3, G6 {};

struct C1 {
   virtual G4& fgrv(int,...);
};

struct C2 : C1 {
   virtual G7& fgrv(int,...);   // C2688, does not return G4&
};
```
