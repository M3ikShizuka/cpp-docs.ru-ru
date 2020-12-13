---
description: 'Дополнительные сведения о: Ошибка компилятора C2272'
title: Ошибка компилятора C2272
ms.date: 11/04/2016
f1_keywords:
- C2272
helpviewer_keywords:
- C2272
ms.assetid: 1517706a-9c27-452e-9b10-3424b3d232bc
ms.openlocfilehash: 5a46c68a09eaec9fc33ef4eaa64afaebea411659
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97336257"
---
# <a name="compiler-error-c2272"></a>Ошибка компилятора C2272

"функция": модификаторы недопустимы для статических функций члена

**`static`** Функция-член объявлена с описателем модели памяти, например [const](../../cpp/const-cpp.md) или [volatile](../../cpp/volatile-cpp.md), и такие модификаторы не допускаются в **`static`** функциях-членах.

Следующий пример приводит к возникновению ошибки C2272:

```cpp
// C2272.cpp
// compile with: /c
class CMyClass {
public:
   static void func1() const volatile;   // C2272  func1 is static
   void func2() const volatile;   // OK
};
```
