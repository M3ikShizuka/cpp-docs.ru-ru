---
description: 'Дополнительные сведения о: Ошибка компилятора C2883'
title: Ошибка компилятора C2883
ms.date: 11/04/2016
f1_keywords:
- C2883
helpviewer_keywords:
- C2883
ms.assetid: 5c6d689d-ed42-41ad-b5c0-e9c2e0b8c356
ms.openlocfilehash: 2ff905f5f1ca8fea4f175799e576e4538bbab164
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97332349"
---
# <a name="compiler-error-c2883"></a>Ошибка компилятора C2883

"имя": объявление функции конфликтует с "идентификатором", представленным с помощью объявления using

Вы попытались определить функцию несколько раз. Первое определение было создано из пространства имен с **`using`** объявлением. Второй является локальным определением.

Следующий пример приводит к возникновению ошибки C2883:

```cpp
// C2883.cpp
namespace A {
   void z(int);
}

int main() {
   using A::z;
   void z(int);   // C2883  z is already defined
}
```
