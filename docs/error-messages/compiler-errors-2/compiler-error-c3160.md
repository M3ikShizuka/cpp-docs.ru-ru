---
description: 'Дополнительные сведения о: Ошибка компилятора C3160'
title: Ошибка компилятора C3160
ms.date: 11/04/2016
f1_keywords:
- C3160
helpviewer_keywords:
- C3160
ms.assetid: a250c433-8adf-43b9-8dee-c3794e09b0a5
ms.openlocfilehash: 863670f30a6a911977ead0d541dcba825e4f124a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97242331"
---
# <a name="compiler-error-c3160"></a>Ошибка компилятора C3160

pointer: данные-член управляемого класса или класса WinRT не могут иметь этот тип

Внутренние указатели сборки мусора могут указывать на внутреннюю часть управляемого класса или класса WinRT. Так как они выполняются медленнее, чем указатели на весь объект, и требуют специальной обработки сборщиком мусора, внутренние управляемые указатели нельзя объявлять как члены класса.

Следующий пример приводит к возникновению ошибки C3160:

```cpp
// C3160.cpp
// compile with: /clr
ref struct A {
   // cannot create interior pointers inside a class
   interior_ptr<int> pg;   // C3160
   int g;   // OK
   int* pg2;   // OK
};

int main() {
   interior_ptr<int> pg2;   // OK
}
```
