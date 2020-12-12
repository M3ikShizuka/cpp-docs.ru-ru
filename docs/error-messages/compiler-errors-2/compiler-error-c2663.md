---
description: 'Дополнительные сведения о: Ошибка компилятора C2663'
title: Ошибка компилятора C2663
ms.date: 11/04/2016
f1_keywords:
- C2663
helpviewer_keywords:
- C2663
ms.assetid: 1e93e368-fd52-42bf-9908-9b6df467c8c9
ms.openlocfilehash: 3e70e2d10b0a133769d92ce637bd9e5f4d44315a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97169987"
---
# <a name="compiler-error-c2663"></a>Ошибка компилятора C2663

"функция": числовые перегрузки не имеют допустимых преобразований для указателя "this"

Компилятору не удалось преобразовать **`this`** в ни одну из перегруженных версий функции члена.

Эта ошибка может быть вызвана вызовом функции, не являющейся **`const`** членом, для **`const`** объекта.  Возможные решения:

1. Удалите **`const`** из объявления объекта.

1. Добавьте **`const`** в одну из перегрузок функции члена.

Следующий пример приводит к возникновению ошибки C2663:

```cpp
// C2663.cpp
struct C {
   void f() volatile {}
   void f() {}
};

struct D {
   void f() volatile;
   void f() const {}
};

const C *pcc;
const D *pcd;

int main() {
   pcc->f();    // C2663
   pcd->f();    // OK
}
```
