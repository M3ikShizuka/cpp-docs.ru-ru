---
description: 'Дополнительные сведения о: Ошибка компилятора C2466'
title: Ошибка компилятора C2466
ms.date: 11/04/2016
f1_keywords:
- C2466
helpviewer_keywords:
- C2466
ms.assetid: 75b251d1-7d0b-4a86-afca-26adedf74486
ms.openlocfilehash: 68ff57de2c0287f24ac84466ac8053bf73f88a95
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97333828"
---
# <a name="compiler-error-c2466"></a>Ошибка компилятора C2466

невозможно выделить массив постоянного размера 0

Массив выделяется или объявляется нулевым размером. Константное выражение для размера массива должно быть целым числом больше нуля. Объявление массива с нулевым индексом является допустимым только для членов класса, структуры или объединения и только с расширениями Майкрософт ([/Ze](../../build/reference/za-ze-disable-language-extensions.md)).

Следующий пример приводит к возникновению ошибки C2466:

```cpp
// C2466.cpp
// compile with: /c
int i[0];   // C2466
int j[1];   // OK
char *p;
```
