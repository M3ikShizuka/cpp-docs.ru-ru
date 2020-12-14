---
description: 'Дополнительные сведения о: Ошибка компилятора C3709'
title: Ошибка компилятора C3709
ms.date: 11/04/2016
f1_keywords:
- C3709
helpviewer_keywords:
- C3709
ms.assetid: d5576b04-2f93-420a-8f3e-8b8e987e8dab
ms.openlocfilehash: 0c884801cc3c720df1018bf7c6d13b13465982a8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97241798"
---
# <a name="compiler-error-c3709"></a>Ошибка компилятора C3709

"функция": неправильный синтаксис для указания события в __hook или \_ _unhook

При указании источника события с [__hook](../../cpp/hook.md) или [__unhook](../../cpp/unhook.md)первым параметром должен быть допустимый метод события, а второй параметр должен быть допустимым объектом источника события (а не методом).

Следующий пример приводит к возникновению ошибки C3709:

```cpp
// C3709.cpp
// compile with: /LD
[event_source(native)]
class CEventSrc
{
public:
   __event void event1();
};

[event_receiver(native)]
class CEventRec
{
public:
   void handler1()
   {
   }

   void HookEvents(CEventSrc* pSrc)
   {
      __hook(bad, pSrc, CEventRec::handler1);   // C3709
      // Try the following line instead:
      // __hook(&CEventSrc::event1, pSrc, CEventRec::handler1);
   }

   void UnhookEvents(CEventSrc* pSrc)
   {
      __unhook(&CEventSrc::event1, pSrc, CEventRec::handler1);
   }
};
```
