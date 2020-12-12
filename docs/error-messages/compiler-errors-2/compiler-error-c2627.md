---
description: 'Дополнительные сведения о: Ошибка компилятора C2627'
title: Ошибка компилятора C2627
ms.date: 11/04/2016
f1_keywords:
- C2627
helpviewer_keywords:
- C2627
ms.assetid: 7fc6c5ac-c7c9-4f0b-ad52-f52252526458
ms.openlocfilehash: 4f09e2b76376871dab93e0736c8a0ca6dbb2b5a6
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97174576"
---
# <a name="compiler-error-c2627"></a>Ошибка компилятора C2627

"функция": функция члена не разрешена в анонимном объединении

[Анонимное объединение](../../cpp/unions.md#anonymous_unions) не может иметь функции элементов.

Следующий пример приводит к возникновению ошибки C2627:

```cpp
// C2627.cpp
int main() {
   union { void f(){} };   // C2627
   union X { void f(){} };
}
```
