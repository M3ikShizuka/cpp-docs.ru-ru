---
description: 'Дополнительные сведения о: Ошибка компилятора C2902'
title: Ошибка компилятора C2902
ms.date: 11/04/2016
f1_keywords:
- C2902
helpviewer_keywords:
- C2902
ms.assetid: 89d78d0e-78e5-4c2c-a0f9-a60110e9395e
ms.openlocfilehash: 45e58615e6bd2465489da7059a350ef476b705a9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97270762"
---
# <a name="compiler-error-c2902"></a>Ошибка компилятора C2902

"токен": непредвиденная лексема после "шаблон", требуется идентификатор

Токен, следующий за ключевым словом, **`template`** не является идентификатором.

Следующий пример приводит к возникновению ошибки C2902:

```cpp
// C2902.cpp
// compile with: /c
namespace N {
   template<class T> class X {};
   class Y {};
}
void g() {
   N::template + 1;   // C2902
}

void f() {
   N::template X<int> x1;   // OK
}
```

Ошибка C2902 также может возникнуть при использовании универсальных шаблонов:

```cpp
// C2902b.cpp
// compile with: /clr /c
namespace N {
   generic<class T> ref class GC {};
}

void f() {
   N::generic + 1;   // C2902
   N::generic GC<int>^ x;
}
```
