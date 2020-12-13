---
description: 'Дополнительные сведения о: Ошибка компилятора C2884'
title: Ошибка компилятора C2884
ms.date: 11/04/2016
f1_keywords:
- C2884
helpviewer_keywords:
- C2884
ms.assetid: 8b4d43e3-3fb5-4360-86c8-de59d8736d4f
ms.openlocfilehash: 008c72ba24bdea260fffc4a49145ecf67c610b15
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97332335"
---
# <a name="compiler-error-c2884"></a>Ошибка компилятора C2884

"имя": появилось при конфликте объявления using с локальной функцией "функция"

Вы попытались определить функцию несколько раз. Первое определение — это локальное определение. Второй — из пространства имен с **`using`** объявлением.

Следующий пример приводит к возникновению ошибки C2884:

```cpp
// C2884.cpp
namespace A {
   void z(int);
}

void f() {
   void z(int);
   using A::z;   // C2884 z is already defined
}
```
