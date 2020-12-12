---
description: 'Дополнительные сведения о: Ошибка компилятора C3865'
title: Ошибка компилятора C3865
ms.date: 11/04/2016
f1_keywords:
- C3865
helpviewer_keywords:
- C3865
ms.assetid: 9bc62bb0-4fb8-4856-a5cf-c7cb4029a596
ms.openlocfilehash: 956cbfeb5bac97cae7e9a9a411c29326062e15b2
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97222883"
---
# <a name="compiler-error-c3865"></a>Ошибка компилятора C3865

"calling_convention": может использоваться только с собственными функциями элементов

Соглашение о вызовах было использовано в функции, которая была глобальной функцией или управляемой функцией-членом. Соглашение о вызовах может использоваться только для собственной (не управляемой) функции-члена.

Дополнительные сведения см. в разделе [соглашения о вызовах](../../cpp/calling-conventions.md).

Следующий пример приводит к возникновению ошибки C3865:

```cpp
// C3865.cpp
// compile with: /clr
// processor: x86
void __thiscall Func(){}   // C3865

// OK
struct MyType {
   void __thiscall Func(){}
};
```
