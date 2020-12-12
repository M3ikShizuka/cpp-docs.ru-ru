---
description: 'Дополнительные сведения о: Ошибка компилятора C3269'
title: Ошибка компилятора C3269
ms.date: 11/04/2016
f1_keywords:
- C3269
helpviewer_keywords:
- C3269
ms.assetid: c575f067-244d-4dd5-bf58-9e7630ea58b7
ms.openlocfilehash: 041a0af061e4ddd1a691c396cdd15e86085124c2
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97113704"
---
# <a name="compiler-error-c3269"></a>Ошибка компилятора C3269

"функция": невозможно объявить функцию-член управляемого или Винрттипе с "..."

Функции-члены управляемого класса и класса WinRT не могут объявлять списки параметров переменной длины.

В следующем примере показано возникновение ошибки C3269 и приводятся сведения по ее устранению.

```cpp
// C3269_2.cpp
// compile with: /clr

ref struct A
{
   void func(int i, ...)   // C3269
   // try the following line instead
   // void func(int i )
   {
   }
};

int main()
{
}
```
