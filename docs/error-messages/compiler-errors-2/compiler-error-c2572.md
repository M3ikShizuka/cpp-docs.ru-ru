---
description: 'Дополнительные сведения о: Ошибка компилятора C2572'
title: Ошибка компилятора C2572
ms.date: 11/04/2016
f1_keywords:
- C2572
helpviewer_keywords:
- C2572
ms.assetid: f1a42d69-727d-4ce5-88c8-d5f55dea66ac
ms.openlocfilehash: ff0549309df0567e2d1d7f26f98f95c3c3b629d5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97208961"
---
# <a name="compiler-error-c2572"></a>Ошибка компилятора C2572

"класс:: член": переопределение параметра по умолчанию: param параметра

Параметры по умолчанию нельзя переопределить. Если для параметра требуется другое значение, параметр по умолчанию должен остаться неопределенным.

Следующий пример приводит к возникновению ошибки C2572:

```cpp
// C2572.cpp
// compile with: /c
void f(int i = 1);   // function declaration

// function definition
void f(int i = 1) {}   // C2572

// try the following line instead
// void f(int i) {}
```
