---
description: 'Дополнительные сведения о: Ошибка компилятора C2602'
title: Ошибка компилятора C2602
ms.date: 11/04/2016
f1_keywords:
- C2602
helpviewer_keywords:
- C2602
ms.assetid: 6c07a40e-537e-4954-b5c5-1e0e58fe1952
ms.openlocfilehash: 2922ee0d35dd5820e1df23d9bc812c0650501b35
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97312025"
---
# <a name="compiler-error-c2602"></a>Ошибка компилятора C2602

"класс:: идентификатор" не является членом базового класса "класс"

`Identifier` не удается получить доступ, так как он не является членом, унаследованным от какого-либо базового класса.

Следующий пример приводит к возникновению ошибки C2602:

```cpp
// C2602.cpp
// compile with: /c
struct X {
   int x;
};
struct A {
   int a;
};
struct B : public A {
   X::x;   // C2602 B is not derived from X
   A::a;   // OK
};
```
