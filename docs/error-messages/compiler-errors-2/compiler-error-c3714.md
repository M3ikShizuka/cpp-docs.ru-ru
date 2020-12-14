---
description: 'Дополнительные сведения о: Ошибка компилятора C3714'
title: Ошибка компилятора C3714
ms.date: 11/04/2016
f1_keywords:
- C3714
helpviewer_keywords:
- C3714
ms.assetid: 17718f75-5a37-4e42-912b-487e91008a95
ms.openlocfilehash: a01544558a156b746c16e731584e30bab7a77825
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97241629"
---
# <a name="compiler-error-c3714"></a>Ошибка компилятора C3714

"метод": метод обработчика событий должен иметь то же соглашение о вызовах, что и исходный "метод"

Был определен метод обработчика событий, который не использовал то же соглашение о вызовах, что и метод исходного события. Чтобы устранить эту ошибку, присвойте методу обработчика событий те же соглашения о вызовах, что и в методе источника события. Например, в приведенном ниже коде производятся соглашения о вызовах `handler1` и `event1` match ([__cdecl](../../cpp/cdecl.md) или [__stdcall](../../cpp/stdcall.md) или другие). Удаление ключевых слов соглашения о вызовах из обоих объявлений позволит устранить проблему, а также присвоить `event1` `handler1` значение по умолчанию соглашению о вызовах [thiscall](../../cpp/thiscall.md) . Дополнительные сведения см. в разделе [соглашения о вызовах](../../cpp/calling-conventions.md) .

Следующий пример приводит к возникновению ошибки C3714:

```cpp
// C3714.cpp
// compile with: /c
// processor: x86
[event_source(native)]
class CEventSrc {
public:
   __event void __cdecl event1();
   // try the following line instead
   // __event void __stdcall event1();
};

[event_receiver(native)]
class CEventRec {
public:
   void __stdcall handler1() {}

   void HookEvents(CEventSrc* pSrc) {
      __hook(&CEventSrc::event1, pSrc, &CEventRec::handler1);   // C3714
   }

   void UnhookEvents(CEventSrc* pSrc) {
      __unhook(&CEventSrc::event1, pSrc, &CEventRec::handler1); // C3714
   }
};
```
