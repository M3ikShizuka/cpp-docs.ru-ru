---
description: 'Дополнительные сведения о: Ошибка компилятора C2723'
title: Ошибка компилятора C2723
ms.date: 11/04/2016
f1_keywords:
- C2723
helpviewer_keywords:
- C2723
ms.assetid: 86925601-2297-4cfd-94e2-2caf27c474c4
ms.openlocfilehash: ab6eacd4279f0fd7b1c44b86b72cbe62ee51020e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97155518"
---
# <a name="compiler-error-c2723"></a>Ошибка компилятора C2723

function: недопустимый описатель specifier в определении функции

Описатель не может использоваться в определении функции вне объявления класса. **`virtual`** Спецификатор может быть указан только в объявлении функции-члена в объявлении класса.

В следующем примере показано возникновение ошибки C2723 и приводятся сведения по ее устранению.

```cpp
// C2723.cpp
struct X {
   virtual void f();
   virtual void g();
};

virtual void X::f() {}   // C2723

// try the following line instead
void X::g() {}
```
