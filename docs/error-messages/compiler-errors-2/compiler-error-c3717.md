---
description: 'Дополнительные сведения о: Ошибка компилятора C3717'
title: Ошибка компилятора C3717
ms.date: 11/04/2016
f1_keywords:
- C3717
helpviewer_keywords:
- C3717
ms.assetid: ae4fceb1-2583-4577-b2f1-40971a017055
ms.openlocfilehash: fecd417af1eceb40ef8b8e48fda40b3ec5e5b36a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97189435"
---
# <a name="compiler-error-c3717"></a>Ошибка компилятора C3717

"метод": метод, порождающий события, не может быть определен

Вы объявили метод события, включающий реализацию. Объявление метода [__event](../../cpp/event.md) не может иметь определения. Чтобы устранить эту ошибку, убедитесь, что объявления методов событий не имеют определений. Например, в приведенном ниже коде удалите тело функции из `event1` объявления, как указано в комментариях.

Следующий пример приводит к возникновению ошибки C3717:

```cpp
// C3717.cpp
[event_source(native)]
class CEventSrc {
public:
   __event void event1() {   // C3717
   }

   // remove definition for event1 and substitute following declaration
   // __event void event1();
};

[event_receiver(native)]
class CEventRec {
public:
   void handler1() {
   }

   void HookEvents(CEventSrc* pSrc) {
      __hook(CEventSrc::event1, pSrc, CEventRec::handler1);
   }

   void UnhookEvents(CEventSrc* pSrc) {
      __unhook(CEventSrc::event1, pSrc, CEventRec::handler1);
   }
};

int main() {
}
```
