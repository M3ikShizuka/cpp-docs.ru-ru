---
description: 'Дополнительные сведения о: Ошибка компилятора C2594'
title: Ошибка компилятора C2594
ms.date: 11/04/2016
f1_keywords:
- C2594
helpviewer_keywords:
- C2594
ms.assetid: 68cd708f-266e-44b0-a211-3e3ab63b11bf
ms.openlocfilehash: 972fb58624a7f2ba185c34f2e58fd9f2dc15217d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97120156"
---
# <a name="compiler-error-c2594"></a>Ошибка компилятора C2594

"оператор": неоднозначные преобразования из "тип1" в "тип2"

Преобразование из *Type1* в *тип2* не было более прямым, чем другое. Мы предлагаем два возможных решения для преобразования из *Type1* в *тип тип2*. Первый вариант — определить прямое преобразование из *Type1* в *тип2*, а второй параметр — указать последовательность преобразований из типа *Type1* в *тип тип2*.

Следующий пример приводит к возникновению ошибки C2594. Предлагаемое разрешение ошибки представляет собой последовательность преобразований.

```cpp
// C2594.cpp
// compile with: /c
struct A{};
struct I1 : A {};
struct I2 : A {};
struct D : I1, I2 {};

A *f (D *p) {
   return (A*) (p);    // C2594

// try the following line instead
// return static_cast<A *>(static_cast<I1 *>(p));
}
```
