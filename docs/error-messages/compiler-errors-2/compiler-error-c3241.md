---
description: 'Дополнительные сведения о: Ошибка компилятора C3241'
title: Ошибка компилятора C3241
ms.date: 11/04/2016
f1_keywords:
- C3241
helpviewer_keywords:
- C3241
ms.assetid: 2ca14879-bba0-4a23-b22a-72cfff92d6a4
ms.openlocfilehash: c940599ccee67338c6a088793970b7a255d83ff2
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97307344"
---
# <a name="compiler-error-c3241"></a>Ошибка компилятора C3241

"метод": Этот метод не был введен с помощью "Interface"

При явном переопределении функции сигнатура функции должна точно совпадать с объявлением переопределяемой функции.

Следующий пример приводит к возникновению ошибки C3241:

```cpp
// C3241.cpp
#pragma warning(disable:4199)

__interface IX12A {
   void mf();
};

__interface IX12B {
   void mf(int);
};

class CX12 : public IX12A, public IX12B { // C3241
   void IX12A::mf(int);
};
```
