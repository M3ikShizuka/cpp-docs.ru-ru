---
description: 'Дополнительные сведения о: Ошибка компилятора C2537'
title: Ошибка компилятора C2537
ms.date: 11/04/2016
f1_keywords:
- C2537
helpviewer_keywords:
- C2537
ms.assetid: aee81d8e-300e-4a8b-b6c4-b3828398b34e
ms.openlocfilehash: 46603ded270b4702d4b7d4de97352547c5f503f8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97302040"
---
# <a name="compiler-error-c2537"></a>Ошибка компилятора C2537

"спецификатор": Недопустимая спецификация компоновки

Возможные причины.

1. Спецификатор компоновки не поддерживается. Поддерживается только описатель компоновки "C".

1. Компоновка "C" указана для более чем одной функции в наборе перегруженных функций. Это не допускается.

Следующий пример приводит к возникновению ошибки C2537:

```cpp
// C2537.cpp
// compile with: /c
extern "c" void func();   // C2537
extern "C" void func2();   // OK
```
