---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 4) C4429'
title: Предупреждение компилятора (уровень 4) C4429
ms.date: 11/04/2016
f1_keywords:
- C4429
helpviewer_keywords:
- C4429
ms.assetid: a3e4cf1f-a869-4e47-834a-850c21eb5297
ms.openlocfilehash: dbd552eb2f8e021f8bf7b7747e2a8aee49bb05a4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97241369"
---
# <a name="compiler-warning-level-4-c4429"></a>Предупреждение компилятора (уровень 4) C4429

возможно, универсальное имя символа неполное или неправильно сформировано

Компилятор обнаружил последовательность символов, которая может быть неправильно сформированным универсальным именем символа. За универсальным именем символа `\u` следуют четыре шестнадцатеричных цифры или `\U` за ними следует восемь шестнадцатеричных цифр.

Следующий пример приводит к возникновению ошибки C4429:

```cpp
// C4429.cpp
// compile with: /W4 /WX
int \ug0e4 = 0;   // C4429
// Try the following line instead:
// int \u00e4 = 0;   // OK, a well-formed universal character name.
```
