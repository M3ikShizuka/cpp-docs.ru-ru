---
description: 'Дополнительные сведения о: Ошибка компилятора C2019'
title: Ошибка компилятора C2019
ms.date: 11/04/2016
f1_keywords:
- C2019
helpviewer_keywords:
- C2019
ms.assetid: 4f37b1e1-9eca-418f-a4c3-141e8512d7b6
ms.openlocfilehash: 5b30bdb8eace513572152d0f33da5f591e21bd6e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97283931"
---
# <a name="compiler-error-c2019"></a>Ошибка компилятора C2019

требуется директива препроцессора, найден "символ"

Символ, за которым следует `#` знак, но не является первой буквой директивы препроцессора.

Следующий пример приводит к возникновению ошибки C2019:

```cpp
// C2019.cpp
#!define TRUE 1   // C2019
```

Возможное решение:

```cpp
// C2019b.cpp
// compile with: /c
#define TRUE 1
```
