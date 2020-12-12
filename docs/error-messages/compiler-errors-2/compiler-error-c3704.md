---
description: 'Дополнительные сведения о: Ошибка компилятора C3704'
title: Ошибка компилятора C3704
ms.date: 11/04/2016
f1_keywords:
- C3704
helpviewer_keywords:
- C3704
ms.assetid: ee40ea35-a214-4dec-9489-d7f155dd0ac2
ms.openlocfilehash: aae489b2d8657a1e62adc654d148be6cd0403af1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97278185"
---
# <a name="compiler-error-c3704"></a>Ошибка компилятора C3704

"функция": метод vararg не может порождать события

Предпринята попытка использовать [__event](../../cpp/event.md) в методе vararg. Чтобы устранить эту ошибку, замените `fireEvent(int i, ...)` вызов `fireEvent(int i)` вызовом, как показано в следующем примере кода.

Следующий пример приводит к возникновению ошибки C3704:

```cpp
// C3704.cpp
[ event_source(native) ]
class CEventSrc {
   public:
      __event void fireEvent(int i, ...);   // C3704
      // try the following line instead:
      // __event void fireEvent(int i);
};

int main() {
}
```
