---
description: 'Дополнительные сведения о: Ошибка компилятора C3739'
title: Ошибка компилятора C3739
ms.date: 11/04/2016
f1_keywords:
- C3739
helpviewer_keywords:
- C3739
ms.assetid: acffe894-08b8-4bf2-9249-9501e6e2bad3
ms.openlocfilehash: dd08b171503d7c5c4c7d46b9d06d4372513e2e73
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97340298"
---
# <a name="compiler-error-c3739"></a>Ошибка компилятора C3739

"класс": синтаксис поддерживается только в том случае, если параметр "layout_dependent" event_receiver имеет значение true

Вы попытались подключить весь интерфейс событий, но `layout_dependent` на [event_receiver](../../windows/attributes/event-receiver.md) атрибут не имеет значения true; необходимо одновременно присоединить одно событие.

Следующий пример приводит к возникновению ошибки C3739:

```cpp
// C3739.cpp
struct A
{
   __event void e();
};

// event_receiver is implied
// [ event_receiver(layout_dependent=false)]

// use the following line instead
// [event_receiver(com, layout_dependent=true), coclass ]
struct B
{
   void f();
   B(A* a)
   {
      __hook(A, a, &B::f);   // C3739
      // use the following line instead to hook a single event
      // __hook(&A::e, a, &B::f);
   }
};

int main()
{
}
```
