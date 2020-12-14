---
description: 'Дополнительные сведения о: Ошибка компилятора C3142'
title: Ошибка компилятора C3142
ms.date: 11/04/2016
f1_keywords:
- C3142
helpviewer_keywords:
- C3142
ms.assetid: 795137ad-d00a-4a9c-9665-0cd8bfb5da8b
ms.openlocfilehash: b03f6efbbf473493354742ef7654e5629b5e5fba
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97204047"
---
# <a name="compiler-error-c3142"></a>Ошибка компилятора C3142

"property_name": невозможно получить адрес свойства

Адрес свойства недоступен для разработчика.

Следующий пример приводит к возникновению ошибки C3142:

```cpp
// C3142_2.cpp
// compile with: /clr
using namespace System;
ref class CSize {
private:
   property int Size {
      int get();
   }
};

int main() {
    &CSize::Size; // C3142
}
```
