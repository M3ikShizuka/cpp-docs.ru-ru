---
description: 'Дополнительные сведения о: Ошибка компилятора C2784'
title: Ошибка компилятора C2784
ms.date: 11/04/2016
f1_keywords:
- C2784
helpviewer_keywords:
- C2784
ms.assetid: 3d761fe2-881c-48bd-afae-e2e714e20473
ms.openlocfilehash: dcee0cc2c6c8154bafe4a37fe83c66b1c8d477d0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97297919"
---
# <a name="compiler-error-c2784"></a>Ошибка компилятора C2784

declaration: не удалось вывести аргумент шаблона для type из type

Компилятор не может определить аргумент шаблона на основе представленных аргументов функции.

В следующем примере показано возникновение ошибки C2784 и приводятся сведения по ее устранению.

```cpp
// C2784.cpp
template<class T> class X {};
template<class T> void f(X<T>) {}

int main() {
   X<int> x;
   f(1);   // C2784

   // To fix it, try the following line instead
   f(x);
}
```
