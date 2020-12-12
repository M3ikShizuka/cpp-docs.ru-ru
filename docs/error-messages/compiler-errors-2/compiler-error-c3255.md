---
description: 'Дополнительные сведения о: Ошибка компилятора C3255'
title: Ошибка компилятора C3255
ms.date: 11/04/2016
f1_keywords:
- C3255
helpviewer_keywords:
- C3255
ms.assetid: 877ffca2-fd92-44b6-9060-6091b928b1c1
ms.openlocfilehash: 576b2c9126173f72470a6e741dd64d8a356c9224
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97194206"
---
# <a name="compiler-error-c3255"></a>Ошибка компилятора C3255

"тип значения": невозможно динамически выделить этот объект типа значения в собственной куче

Экземпляры типа значения (см. [классы и структуры](../../extensions/classes-and-structs-cpp-component-extensions.md)), содержащие управляемые элементы, могут быть созданы в стеке, но не в куче.

Следующий пример приводит к возникновению ошибки C3255:

```cpp
// C3255.cpp
// compile with: /clr
using namespace System;
value struct V {
   Object^ o;
};

value struct V2 {
   int i;
};

int main() {
   V* pv = new V;   // C3255
   V2* pv2 = new V2;
   V v2;
}
```
