---
description: 'Дополнительные сведения о: Ошибка компилятора C3609'
title: Ошибка компилятора C3609
ms.date: 11/04/2016
f1_keywords:
- C3609
helpviewer_keywords:
- C3609
ms.assetid: 801e7f79-4ac6-4f8f-955f-703cdf095d00
ms.openlocfilehash: 187bc6d9849c385f6adb3ae2c25e2e90e7393e6e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97223130"
---
# <a name="compiler-error-c3609"></a>Ошибка компилятора C3609

member: запечатанная или окончательная функция должна быть виртуальной

[Запечатанные](../../extensions/sealed-cpp-component-extensions.md) и [окончательные](../../cpp/final-specifier.md) ключевые слова разрешены только для класса, структуры или функции-члена, помеченной как **`virtual`** .

Следующий пример приводит к возникновению ошибки C3609:

```cpp
// C3609.cpp
// compile with: /clr /c
ref class C {
   int f() sealed;   // C3609
   virtual int f2() sealed;   // OK
};
```
