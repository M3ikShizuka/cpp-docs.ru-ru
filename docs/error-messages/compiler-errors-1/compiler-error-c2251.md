---
description: 'Дополнительные сведения о: Ошибка компилятора C2251'
title: Ошибка компилятора C2251
ms.date: 11/04/2016
f1_keywords:
- C2251
helpviewer_keywords:
- C2251
ms.assetid: fefe050c-f8d3-4316-b237-8007dbcdd3bf
ms.openlocfilehash: 029d6fc807757da14cf004b4bf1d8ae253f17ec7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97134814"
---
# <a name="compiler-error-c2251"></a>Ошибка компилятора C2251

в пространстве имен "пространство_имен" отсутствует член "член" — имелся в виду "член"?

Компилятору не удалось обнаружить идентификатор в указанном пространстве имен.

В следующем примере возникает ошибка C2251:

```cpp
// C2251.cpp
// compile with: /c
namespace A {
   namespace B {
      void f1();
   }

   using namespace B;
}

void A::f1() {}   // C2251
void A::B::f1() {}   // OK
```
