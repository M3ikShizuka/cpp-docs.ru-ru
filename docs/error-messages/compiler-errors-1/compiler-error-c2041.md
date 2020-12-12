---
description: 'Дополнительные сведения о: Ошибка компилятора C2041'
title: Ошибка компилятора C2041
ms.date: 11/04/2016
f1_keywords:
- C2041
helpviewer_keywords:
- C2041
ms.assetid: c9a33bb1-f9cf-47d6-bd21-7d867a8c37d5
ms.openlocfilehash: 5c980b6783b4b14e4878278699e5b4f7618ff0f8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97175265"
---
# <a name="compiler-error-c2041"></a>Ошибка компилятора C2041

недопустимая цифра "символ" для основания "Number"

Указанный символ не является допустимой цифрой для основания (например, восьмеричной или шестнадцатеричной).

Следующий пример приводит к возникновению ошибки C2041:

```cpp
// C2041.cpp
int i = 081;   // C2041  8 is not a base 8 digit
```

Возможное решение:

```cpp
// C2041b.cpp
// compile with: /c
int j = 071;
```
