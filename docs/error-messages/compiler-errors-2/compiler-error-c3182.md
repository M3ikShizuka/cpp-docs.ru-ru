---
description: 'Дополнительные сведения о: Ошибка компилятора C3182'
title: Ошибка компилятора C3182
ms.date: 11/04/2016
f1_keywords:
- C3182
helpviewer_keywords:
- C3182
ms.assetid: f3681266-308e-4990-a979-8eef8920e186
ms.openlocfilehash: d4cf5d86a553a597636c09f72ff3a068e2a6b9b2
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97242032"
---
# <a name="compiler-error-c3182"></a>Ошибка компилятора C3182

"класс": объявление члена с использованием объявления или доступа недопустимо в управляемом или Винрттипе

Объявление [using](../../cpp/using-declaration.md) является недопустимым во всех формах управляемых классов.

В следующем примере показано возникновение ошибки C3182 и приводятся сведения по ее устранению.

```cpp
// C3182a.cpp
// compile with: /clr /c
ref struct B {
   void mf(int) {
   }
};

ref struct D : B {
   using B::mf;   // C3182, delete to resolve
   void mf(char) {
   }
};
```
