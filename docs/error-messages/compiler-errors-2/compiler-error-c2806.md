---
description: 'Дополнительные сведения о: Ошибка компилятора C2806'
title: Ошибка компилятора C2806
ms.date: 11/04/2016
f1_keywords:
- C2806
helpviewer_keywords:
- C2806
ms.assetid: 7c9ff1f4-1590-4c47-991d-b1075a173b48
ms.openlocfilehash: ba215bdb5293644cc9d655055c2cc44da5de7add
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97320670"
---
# <a name="compiler-error-c2806"></a>Ошибка компилятора C2806

"operator оператор" имеет слишком много формальных параметров

Перегруженный оператор имеет слишком много параметров.

Следующий пример приводит к возникновению ошибки C2806:

```cpp
// C2806.cpp
// compile with: /c
class X {
public:
   X operator++ ( int, int );   // C2806 more than 1 parameter
   X operator++ ( int );   // OK
} ;
```
