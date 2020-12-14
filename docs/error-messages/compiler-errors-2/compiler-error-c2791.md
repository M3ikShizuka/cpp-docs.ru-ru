---
description: 'Дополнительные сведения о: Ошибка компилятора C2791'
title: Ошибка компилятора C2791
ms.date: 11/04/2016
f1_keywords:
- C2791
helpviewer_keywords:
- C2791
ms.assetid: 938ad1fb-75d9-4ce2-ad92-83d6249005b5
ms.openlocfilehash: 0f5bd93c1c6ee32399da793147a18e9225b5fcb1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97297776"
---
# <a name="compiler-error-c2791"></a>Ошибка компилятора C2791

Недопустимое использование "Super": "класс" не имеет базовых классов

Ключевое слово [Super](../../cpp/super.md) было использовано в контексте функции-члена класса, не имеющего базовых классов.

Следующий пример приводит к возникновению ошибки C2791:

```cpp
// C2791.cpp
struct D {
   void mf() {
      __super::mf();   // C2791
   }
};
```
