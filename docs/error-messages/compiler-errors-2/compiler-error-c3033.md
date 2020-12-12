---
description: 'Дополнительные сведения о: Ошибка компилятора C3033'
title: Ошибка компилятора C3033
ms.date: 11/04/2016
f1_keywords:
- C3033
helpviewer_keywords:
- C3033
ms.assetid: 8628b6bb-a650-4ed2-af13-57acd2f7ddbb
ms.openlocfilehash: 999cedd270470bde27a57be0159eedda61297092
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97270242"
---
# <a name="compiler-error-c3033"></a>Ошибка компилятора C3033

"переменная": переменная в предложении "предложение" не может иметь тип, квалифицированный как const

Значения, передаваемые в определенные предложения, не могут быть **`const`** переменными.

Следующий пример приводит к возникновению ошибки C3033:

```cpp
// C3033.cpp
// compile with: /openmp /link vcomps.lib
int main() {
   const int val = 1;
   int val2 = 1;

   #pragma omp parallel reduction(+ : val)   // C3033
   ;

   #pragma omp parallel reduction(+ : val2)   // OK
   ;
}
```
