---
description: 'Дополнительные сведения о: Ошибка компилятора C3743'
title: Ошибка компилятора C3743
ms.date: 11/04/2016
f1_keywords:
- C3743
helpviewer_keywords:
- C3743
ms.assetid: 7ca9a76e-7b60-46d1-ab8b-18600cf1a306
ms.openlocfilehash: 1afad204f25220df53d58313a5742424e3491710
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97340246"
---
# <a name="compiler-error-c3743"></a>Ошибка компилятора C3743

можно только подключить или отсоединить весь интерфейс, если параметр "layout_dependent" event_receiver имеет значение true

Функция [__unhook](../../cpp/unhook.md) зависит от числа параметров, которые она принимает, в зависимости от значения, переданного в `layout_dependent` параметр класса [event_receiver](../../windows/attributes/event-receiver.md) .

Следующий пример приводит к возникновению ошибки C3743:

```cpp
// C3743.cpp
#define _ATL_ATTRIBUTES 1
#include <atlbase.h>
#include <atlcom.h>
[module(name="xx")];
[object] __interface I { HRESULT f(); };

[event_receiver(com, layout_dependent=true), coclass]
struct R : I {
        HRESULT f() {
      return 0;
   }
        R() {
   }

   R(I* a) {
      __hook(I, a, &R::f);   // C3743
      // The following line resolves the error.
      // __hook(I, a);
   }
};
```
