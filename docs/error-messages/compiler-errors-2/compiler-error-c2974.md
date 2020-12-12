---
description: 'Дополнительные сведения о: Ошибка компилятора C2974'
title: Ошибка компилятора C2974
ms.date: 11/04/2016
f1_keywords:
- C2974
helpviewer_keywords:
- C2974
ms.assetid: 1b444260-f2bf-48d7-ab1e-35573d8c4a0e
ms.openlocfilehash: 0f6d455a2ca79c4c830b24641a894356a5ef04b9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97210365"
---
# <a name="compiler-error-c2974"></a>Ошибка компилятора C2974

Недопустимый аргумент типа "Number", требуется тип

Универсальный аргумент или параметр шаблона не соответствует универсальному объявлению или шаблону. Тип должен находиться в угловых скобках. Проверьте определение универсального типа или шаблона, чтобы найти правильные типы.

Следующий пример приводит к возникновению ошибки C2974:

```cpp
// C2974.cpp
// C2974 expected
template <class T>
struct TC {};

template <typename T>
void tf(T){}

int main() {
   // Delete the following 2 lines to resolve
   TC<1>* tc;
   tf<"abc">("abc");

   TC<int>* tc;
   tf<const char *>("abc");
}
```

C2974 также может возникать при использовании универсальных шаблонов:

```cpp
// C2974b.cpp
// compile with: /clr
// C2974 expected
using namespace System;
generic <class T>
ref struct GCtype {};

generic <typename T>
void gf(T){}

int main() {
   // Delete the following 2 lines to resolve
   GCtype<"a">^ gc;
   gf<"a">("abc");

   // OK
   GCtype<int>^ gc;
   gf<String ^>("abc");
}
```
