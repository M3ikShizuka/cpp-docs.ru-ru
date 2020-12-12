---
description: 'Дополнительные сведения о: Ошибка компилятора C3032'
title: Ошибка компилятора C3032
ms.date: 11/04/2016
f1_keywords:
- C3032
helpviewer_keywords:
- C3032
ms.assetid: 6a92bd8e-319f-4a99-aef4-a9021f6f9928
ms.openlocfilehash: 18bae374cd5bf475c4cd791fce45a30fc8465739
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97270268"
---
# <a name="compiler-error-c3032"></a>Ошибка компилятора C3032

"переменная": переменная в предложении "предложение" не может быть неполного типа "тип"

Типы, переданные в некоторые предложения, должны быть полностью видимы для компилятора.

При компиляции следующего примера возникнет ошибка C3032:

```cpp
// C3032.cpp
// compile with: /openmp /link vcomps.lib
#include "omp.h"

struct Incomplete;
extern struct Incomplete inc;

int main() {
   int i = 9;
   #pragma omp parallel private(inc)   // C3032
      ;

   #pragma omp parallel private(i)     // OK
      ;

}
```
