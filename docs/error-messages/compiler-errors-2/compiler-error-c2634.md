---
description: 'Дополнительные сведения о: Ошибка компилятора C2634'
title: Ошибка компилятора C2634
ms.date: 11/04/2016
f1_keywords:
- C2634
helpviewer_keywords:
- C2634
ms.assetid: 58c8f2db-ac95-4a81-9355-ef3cfb0ba7b3
ms.openlocfilehash: 5e8aee2ce27fc56f1204d925147f48352bd24a15
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97123413"
---
# <a name="compiler-error-c2634"></a>Ошибка компилятора C2634

"&класс:: член": недопустимый указатель на ссылочный член

Объявлен указатель на ссылочный член.

Следующий пример приводит к возникновению ошибки C2634:

```cpp
// C2634.cpp
int mem;
struct S {
   S() : rf(mem) { }
   int &rf;
};
int (S::*pdm) = &S::rf;   // C2634
```
