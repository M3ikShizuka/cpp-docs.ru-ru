---
description: 'Дополнительные сведения о: Ошибка компилятора C2556'
title: Ошибка компилятора C2556
ms.date: 11/04/2016
f1_keywords:
- C2556
helpviewer_keywords:
- C2556
ms.assetid: fc4399ad-45b3-49fd-be1f-0b13956a595a
ms.openlocfilehash: 6c2233e10e763e959511c6b435e0d894e921905a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97134489"
---
# <a name="compiler-error-c2556"></a>Ошибка компилятора C2556

"идентификатор": перегруженные функции отличаются только типом возвращаемого значения

Перегруженные функции имеют различные возвращаемые типы, но один и тот же список параметров. Каждая перегруженная функция должна иметь отдельный список формальных параметров.

Следующий пример приводит к возникновению ошибки C2556:

```cpp
// C2556.cpp
// compile with: /c
class C {
   int func();
   double func();   // C2556
   int func(int i);   // ok parameter lists differ
};
```
