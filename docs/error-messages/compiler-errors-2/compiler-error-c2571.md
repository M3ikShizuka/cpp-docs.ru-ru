---
description: 'Дополнительные сведения о: Ошибка компилятора C2571'
title: Ошибка компилятора C2571
ms.date: 11/04/2016
f1_keywords:
- C2571
helpviewer_keywords:
- C2571
ms.assetid: c6522616-dee9-4d7d-9bf8-30a7e1deaadf
ms.openlocfilehash: 773cab05204e15a22a4412364bd8f89cddfd92ea
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97208974"
---
# <a name="compiler-error-c2571"></a>Ошибка компилятора C2571

"функция": виртуальная функция не может находиться в Union "Union"

Объединение объявляется с помощью виртуальной функции. Виртуальную функцию можно объявить только в классе или структуре.  Возможные решения:

1. Измените объединение на класс или структуру.

1. Сделайте функцию невиртуальной.

Следующий пример приводит к возникновению ошибки C2571:

```cpp
// C2571.cpp
// compile with: /c
union A {
   virtual void func1();   // C2571
   void func2();   // OK
};
```
