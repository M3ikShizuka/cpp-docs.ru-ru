---
description: 'Дополнительные сведения о: Ошибка компилятора C2391'
title: Ошибка компилятора C2391
ms.date: 11/04/2016
f1_keywords:
- C2391
helpviewer_keywords:
- C2391
ms.assetid: 63a9c6b9-03cc-4517-885c-bdcd048643b3
ms.openlocfilehash: 3161cd6ade15817142cc24f38c61fd3e09eb8857
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97337580"
---
# <a name="compiler-error-c2391"></a>Ошибка компилятора C2391

"идентификатор": "Friend" не может использоваться во время определения типа

**`friend`** Объявление содержит полное объявление класса. **`friend`** Объявление может указывать функцию-член или настраиваемый спецификатор типа, но не полное объявление класса.

При компиляции следующего примера возникнет ошибка C2326:

```cpp
// C2391.cpp
// compile with: /c
class D {
   void func( int );
};

class A {
   friend class B { int i; };   // C2391

   // OK
   friend class C;
   friend void D::func(int);
};
```
