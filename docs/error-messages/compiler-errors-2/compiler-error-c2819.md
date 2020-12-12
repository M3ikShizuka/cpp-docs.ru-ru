---
description: 'Дополнительные сведения о: Ошибка компилятора C2819'
title: Ошибка компилятора C2819
ms.date: 11/04/2016
f1_keywords:
- C2819
helpviewer_keywords:
- C2819
ms.assetid: fcc7762d-cb82-4bb1-a715-0d82da832edf
ms.openlocfilehash: fa30432399913c6bdd00bb2728931d213c14064c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97194752"
---
# <a name="compiler-error-c2819"></a>Ошибка компилятора C2819

тип "тип" не имеет перегруженного члена "operator->"

Необходимо определить, `operator->()` чтобы использовать эту операцию с указателями.

Следующий пример приводит к возникновению ошибки C2819:

```cpp
// C2819.cpp
// compile with: /c
class A {
   public:
      int i;
};

class B {};

void C(B j) {
   j->i;   // C2819
}

class D {
   A* pA;

   public:
      A* operator->() {
         return pA;
      }
};

void F(D j) {
   j->i;
}
```

C2819 также может возникать при использовании [семантики стека C++ для ссылочных типов](../../dotnet/cpp-stack-semantics-for-reference-types.md). Следующий пример приводит к возникновению ошибки C2819:

```cpp
// C2819_b.cpp
// compile with: /clr
ref struct R {
   void Test() {}
};

int main() {
   R r;
   r->Test();   // C2819
   r.Test();   // OK
}
```
