---
description: 'Дополнительные сведения о: Ошибка компилятора C2313'
title: Ошибка компилятора C2313
ms.date: 11/04/2016
f1_keywords:
- C2313
helpviewer_keywords:
- C2313
ms.assetid: f70eb19b-c0a3-4fb2-ade1-3890a589928d
ms.openlocfilehash: 455bc3a833f576c051ff1531d921f8504789810e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97282162"
---
# <a name="compiler-error-c2313"></a>Ошибка компилятора C2313

"тип1": перехват по ссылке ("тип2") в строке "номер"

Тип исключения имеет два обработчика. Тип второго перехвата — это ссылка на тип первого перехвата.

В следующем примере возникает ошибка C2313:

```cpp
// C2313.cpp
// compile with: /EHsc
#include <eh.h>
class C {};
int main() {
    try {
        throw "ooops!";
    }
    catch( C& ) {}
    catch( C ) {}   // C2313
}
```
