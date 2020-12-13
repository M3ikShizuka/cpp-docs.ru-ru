---
description: 'Дополнительные сведения о: Ошибка компилятора C2758'
title: Ошибка компилятора C2758
ms.date: 11/04/2016
f1_keywords:
- C2758
helpviewer_keywords:
- C2758
ms.assetid: 1d273034-194c-4926-9869-142d1b219cbe
ms.openlocfilehash: 28ca42a5dc62ad17fef59ca129092f791a12a39f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97336174"
---
# <a name="compiler-error-c2758"></a>Ошибка компилятора C2758

member: требуется инициализация члена ссылочного типа

Ошибка компилятора C2758 возникает, если конструктор не инициализирует член ссылочного типа в списке инициализаторов. Компилятор оставляет член неопределенным. Переменные ссылочного члена должны инициализироваться при объявлении или получать значение в списке инициализации конструктора.

Следующий пример приводит к возникновению ошибки C2758:

```cpp
// C2758.cpp
// Compile by using: cl /W3 /c C2758.cpp
struct A {
   const int i;

   A(int n) { };   // C2758
   // try the following line instead
   // A(int n) : i{n} {};
};
```
