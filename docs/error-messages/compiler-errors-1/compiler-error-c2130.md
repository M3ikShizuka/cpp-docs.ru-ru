---
description: 'Дополнительные сведения о: Ошибка компилятора C2130'
title: Ошибка компилятора C2130
ms.date: 11/04/2016
f1_keywords:
- C2130
helpviewer_keywords:
- C2130
ms.assetid: c6fd5a7e-8f28-4f67-99d1-95a13b0dff90
ms.openlocfilehash: 78e7b756d5902562c6093e3f26f9934e87e732ff
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97323185"
---
# <a name="compiler-error-c2130"></a>Ошибка компилятора C2130

\#ожидалась строка, содержащая имя файла, обнаружено "token"

Дополнительный токен имени файла после директивы [#line](../../preprocessor/hash-line-directive-c-cpp.md) `linenumber` должен быть строкой.

При компиляции следующего примера возникнет ошибка C2130:

```cpp
// C2130.cpp
int main() {
   #line 1000 test   // C2130
   #line 1000 "test"   // OK
}
```
