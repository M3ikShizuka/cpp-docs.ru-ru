---
description: 'Дополнительные сведения о: Ошибка компилятора C3254'
title: Ошибка компилятора C3254
ms.date: 11/04/2016
f1_keywords:
- C3254
helpviewer_keywords:
- C3254
ms.assetid: 93427b10-fa72-4e43-80d1-1a6e122f9f40
ms.openlocfilehash: 7d0084f52060803cd99b973c9f6105fc8915c2aa
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97194219"
---
# <a name="compiler-error-c3254"></a>Ошибка компилятора C3254

"explicit override": класс содержит явное переопределение "override", но не является производным от интерфейса, содержащего объявление функции

При [явном переопределении](../../cpp/explicit-overrides-cpp.md) метода класс, содержащий переопределение, должен прямо или косвенно наследовать от типа, содержащего переопределяемую функцию.

Следующий пример приводит к возникновению ошибки C3254:

```cpp
// C3254.cpp
__interface I
{
   void f();
};

__interface I1 : I
{
};

struct A /* : I1 */
{
   void I1::f()
   {   // C3254, uncomment : I1 to resolve this C3254
   }
};

int main()
{
}
```
