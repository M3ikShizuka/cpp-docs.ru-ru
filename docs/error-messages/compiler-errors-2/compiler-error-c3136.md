---
description: 'Дополнительные сведения о: Ошибка компилятора C3136'
title: Ошибка компилятора C3136
ms.date: 10/03/2018
f1_keywords:
- C3136
helpviewer_keywords:
- C3136
ms.assetid: c77103cd-00f7-408e-b74b-4f8562039d31
ms.openlocfilehash: 4203eaa1f41603075bbb8162b7156783c8f2680a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97239380"
---
# <a name="compiler-error-c3136"></a>Ошибка компилятора C3136

"Interface": COM-интерфейс может наследовать только от другого COM-интерфейса, "Interface" не является COM-интерфейсом

Интерфейс, к которому был применен [атрибут интерфейса](../../windows/attributes/interface-attributes.md) , наследуется от интерфейса, который не является COM-интерфейсом. Интерфейс COM в конечном итоге наследует от `IUnknown` . Любой интерфейс, которому предшествует атрибут Interface, является COM-интерфейсом.

Следующий пример приводит к возникновению ошибки C3136:

```cpp
// C3136.cpp
#include "unknwn.h"

__interface A   // C3136
// try the following line instead
// _interface A : IUnknown
{
   int a();
};

[object]
__interface B : A
{
   int aa();
};
```
