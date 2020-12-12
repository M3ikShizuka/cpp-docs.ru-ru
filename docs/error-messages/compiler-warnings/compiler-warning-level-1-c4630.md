---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4630'
title: Предупреждение компилятора (уровень 1) C4630
ms.date: 11/04/2016
f1_keywords:
- C4630
helpviewer_keywords:
- C4630
ms.assetid: d8926376-7acc-4fc7-8438-6f0de3468870
ms.openlocfilehash: 49a73dcd3ce11fefa1d4275e57ad98092c242d8d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97318914"
---
# <a name="compiler-warning-level-1-c4630"></a>Предупреждение компилятора (уровень 1) C4630

"символ": спецификатор класса хранения "extern" недопустим для определения члена

Элемент данных или функция-член определяется как **`extern`** . Элементы не могут быть внешними, хотя все объекты могут. Компилятор игнорирует **`extern`** ключевое слово. Следующий пример приводит к возникновению ошибки C4630:

```cpp
// C4630.cpp
// compile with: /W1 /LD
class A {
   void func();
};

extern void A::func() {   // C4630, remove 'extern' to resolve
}
```
