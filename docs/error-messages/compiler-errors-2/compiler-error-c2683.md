---
description: 'Дополнительные сведения о: Ошибка компилятора C2683'
title: Ошибка компилятора C2683
ms.date: 11/04/2016
f1_keywords:
- C2683
helpviewer_keywords:
- C2683
ms.assetid: db605e4f-601b-4d05-92a1-c43ca24de08d
ms.openlocfilehash: 9cb13204163370ea529c88cc5648a25a4e520370
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97220777"
---
# <a name="compiler-error-c2683"></a>Ошибка компилятора C2683

"CAST": "тип" не является полиморфизмом типа

Нельзя использовать [dynamic_cast](../../cpp/dynamic-cast-operator.md) для преобразования из неполиморфизмного класса (класса без виртуальных функций).

[Static_cast](../../cpp/static-cast-operator.md) можно использовать для выполнения преобразований неполиморфизмных типов. Однако не **`static_cast`** выполняет проверку во время выполнения.

Следующий пример приводит к возникновению ошибки C2683:

```cpp
// C2683.cpp
// compile with: /c
class B { };
class D : public B { };

void f(B* pb) {
   D* pd1 = dynamic_cast<D*>(pb);  // C2683
   D* pd1 = static_cast<D*>(pb);   // OK
}
```
