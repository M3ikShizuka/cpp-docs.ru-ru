---
description: 'Дополнительные сведения о: Ошибка компилятора C2093'
title: Ошибка компилятора C2093
ms.date: 11/04/2016
f1_keywords:
- C2093
helpviewer_keywords:
- C2093
ms.assetid: 17529a70-9169-46b5-9fc6-57a5ce224e6a
ms.openlocfilehash: d08c2e29415363fc64309a89691ec0852ca5fa88
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97251860"
---
# <a name="compiler-error-c2093"></a>Ошибка компилятора C2093

"variable1": невозможно инициализировать с помощью адреса автоматической переменной "variable2"

При компиляции с параметром [/Za](../../build/reference/za-ze-disable-language-extensions.md)программа попыталась использовать адрес автоматической переменной в качестве инициализатора.

Следующий пример приводит к возникновению ошибки C2093:

```c
// C2093.c
// compile with: /Za /c
void func() {
   int li;   // an implicit auto variable
   int * s[]= { &li };   // C2093 address is not a constant

   // OK
   static int li2;
   int * s2[]= { &li2 };
}
```
