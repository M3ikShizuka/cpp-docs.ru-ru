---
description: 'Дополнительные сведения о: Ошибка компилятора C3270'
title: Ошибка компилятора C3270
ms.date: 11/04/2016
f1_keywords:
- C3270
helpviewer_keywords:
- C3270
ms.assetid: 70e6e76b-7415-48f5-a61e-2ed50caf08e4
ms.openlocfilehash: 976e4c9e6b1448c01b58b754d6ca4a09a1607fbf
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97185899"
---
# <a name="compiler-error-c3270"></a>Ошибка компилятора C3270

"поле": атрибут FieldOffset можно использовать только в контексте StructLayout(Explicit), в котором он обязателен

Поле было отмечено с помощью **FieldOffset**, что допускается только в том случае, если действует **StructLayout (explicit)** .

Следующий пример приводит к возникновению ошибки C3270:

```cpp
// C3270_2.cpp
// compile with: /clr /c
using namespace System::Runtime::InteropServices;

[ StructLayout(LayoutKind::Sequential) ]
// try the following line instead
// [ StructLayout(LayoutKind::Explicit) ]
public value struct MYUNION
{
   [FieldOffset(0)] int a;   // C3270
   // ...
};
```
