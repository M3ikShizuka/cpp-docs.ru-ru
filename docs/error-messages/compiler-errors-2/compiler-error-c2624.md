---
description: 'Дополнительные сведения о: Ошибка компилятора C2624'
title: Ошибка компилятора C2624
ms.date: 11/04/2016
f1_keywords:
- C2624
helpviewer_keywords:
- C2624
ms.assetid: 32f2ec15-a7cd-4049-a64b-131746d3152b
ms.openlocfilehash: 4fa52e5192bd71c9fcdd3608b4161d1e5da57bdf
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97174680"
---
# <a name="compiler-error-c2624"></a>Ошибка компилятора C2624

локальные классы нельзя использовать для объявления переменных "extern"

Для объявления переменных нельзя использовать локальный класс или структуру **`extern`** .

Следующий пример приводит к возникновению ошибки C2624:

```cpp
// C2624.cpp
int main() {
   struct C {};
   extern C ac;   // C2624
}
```
