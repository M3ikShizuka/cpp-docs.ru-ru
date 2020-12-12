---
description: 'Дополнительные сведения о: Ошибка компилятора C2574'
title: Ошибка компилятора C2574
ms.date: 11/04/2016
f1_keywords:
- C2574
helpviewer_keywords:
- C2574
ms.assetid: 3e1c5c18-ee8b-4dbb-bfc0-d3b8991af71b
ms.openlocfilehash: 361cc52f2a76e5470109db07ccabbe6d78291a43
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97208896"
---
# <a name="compiler-error-c2574"></a>Ошибка компилятора C2574

"деструктор": невозможно объявить как статический

Деструкторы и конструкторы не могут быть объявлены **`static`** .

Следующий пример приводит к возникновению ошибки C2574:

```cpp
// C2574.cpp
// compile with: /c
class A {
   virtual static ~A();   // C2574
   //  try the following line instead
   // virtual ~A();
};
```
