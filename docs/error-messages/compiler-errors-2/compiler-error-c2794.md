---
description: 'Дополнительные сведения о: Ошибка компилятора C2794'
title: Ошибка компилятора C2794
ms.date: 11/04/2016
f1_keywords:
- C2794
helpviewer_keywords:
- C2794
ms.assetid: d508191c-9044-4c6a-9119-4bca668c0b93
ms.openlocfilehash: 68f0c20e7942a32ede42fa8d7d069164d083377a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97297659"
---
# <a name="compiler-error-c2794"></a>Ошибка компилятора C2794

"функция": не является членом какого-либо прямого или косвенного базового класса "класс"

Вы попытались использовать [Super](../../cpp/super.md) для вызова несуществующей функции-члена.

Следующий пример приводит к возникновению ошибки C2794

```cpp
// C2794.cpp
struct B {
   void mf();
};

struct D : B {
   void mf() {
      __super::f();  // C2794
   }
};
```
