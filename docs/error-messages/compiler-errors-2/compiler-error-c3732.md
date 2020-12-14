---
description: 'Дополнительные сведения о: Ошибка компилятора C3732'
title: Ошибка компилятора C3732
ms.date: 11/04/2016
f1_keywords:
- C3732
helpviewer_keywords:
- C3732
ms.assetid: 2d55a7e1-9c39-4379-a093-2f7beb27e2ca
ms.openlocfilehash: 406acf356ee0bec09eb5d9e218114256f9c58858
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97245061"
---
# <a name="compiler-error-c3732"></a>Ошибка компилятора C3732

"интерфейс": Пользовательский интерфейс, порождающий COM-события, не может наследовать от IDispatch

Интерфейс, который поддерживает события COM, не может наследовать от `IDispatch` . Дополнительные сведения см. [в разделе Обработка событий в com](../../cpp/event-handling-in-com.md).

Следующая ошибка создает C3732:

```cpp
// C3732.cpp
#define _ATL_ATTRIBUTES 1
#include "atlbase.h"
#include "atlcom.h"

[module(name="test")];

// to resolve this C3732, use dual instead of object
// or inherit from IUnknown
[ object ]
__interface I : IDispatch
{
};

[ event_source(com), coclass ]
struct A
{
   __event __interface I;   // C3732
};

int main()
{
}
```
