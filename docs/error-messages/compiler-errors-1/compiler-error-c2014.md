---
description: 'Дополнительные сведения о: Ошибка компилятора C2014'
title: Ошибка компилятора C2014
ms.date: 11/04/2016
f1_keywords:
- C2014
helpviewer_keywords:
- C2014
ms.assetid: 231d8e9c-48c0-4027-99a3-245d186275ec
ms.openlocfilehash: 2f8de1d2b9ea8ef680826cfbfc189dbe2617c9f6
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97220985"
---
# <a name="compiler-error-c2014"></a>Ошибка компилятора C2014

команда препроцессора должна начинаться как первое непустое пространство

`#`Знак директивы препроцессора должен быть первым символом в строке, которая не является пробелом.

Следующий пример приводит к возникновению ошибки C2014:

```cpp
// C2014.cpp
int k; #include <stdio.h>   // C2014
```

Возможное решение:

```cpp
// C2014b.cpp
// compile with: /c
int k;
#include <stdio.h>
```
