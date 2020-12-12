---
description: 'Дополнительные сведения о: Ошибка компилятора C3892'
title: Ошибка компилятора C3892
ms.date: 11/04/2016
f1_keywords:
- C3892
helpviewer_keywords:
- C3892
ms.assetid: 83fff42c-ea48-442f-bc2e-b33a6b99d890
ms.openlocfilehash: 1fe2692e594debebdaf3493414d0e6136c9403a5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97274272"
---
# <a name="compiler-error-c3892"></a>Ошибка компилятора C3892

"var": невозможно присвоить значение переменной, которая является константой

Переменную const нельзя изменить после ее объявления и инициализации.

Следующий пример приводит к возникновению ошибки C3892:

```cpp
// C3892.cpp
// compile with: /clr
ref struct Y1 {
   static const int staticConst = 9;
};

int main() {
   Y1::staticConst = 0;   // C3892
}
```
