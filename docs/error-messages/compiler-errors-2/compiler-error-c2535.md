---
description: 'Дополнительные сведения о: Ошибка компилятора C2535'
title: Ошибка компилятора C2535
ms.date: 11/04/2016
f1_keywords:
- C2535
helpviewer_keywords:
- C2535
ms.assetid: a958f83e-e2bf-4a59-b44b-d406ec325d7e
ms.openlocfilehash: 149ddabcde7364513379701c55d4801fd403206b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97258087"
---
# <a name="compiler-error-c2535"></a>Ошибка компилятора C2535

"идентификатор": функция члена уже определена или объявлена

Эта ошибка может быть вызвана тем, что один и тот же список формальных параметров используется в нескольких определениях или объявлениях перегруженной функции.

Если вы получаете C2535 из-за функции Dispose, см. Дополнительные сведения о [деструкторах и методах завершения](../../dotnet/how-to-define-and-consume-classes-and-structs-cpp-cli.md#BKMK_Destructors_and_finalizers) .

Следующий пример приводит к возникновению ошибки C2535:

```cpp
// C2535.cpp
// compile with: /c
class C {
public:
   void func();   // forward declaration
   void func() {}   // C2535
};
```
