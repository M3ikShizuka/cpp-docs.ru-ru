---
description: 'Дополнительные сведения о: Ошибка компилятора C2761'
title: Ошибка компилятора C2761
ms.date: 11/04/2016
f1_keywords:
- C2761
helpviewer_keywords:
- C2761
ms.assetid: 38c79a05-b56d-485b-820f-95e8c0cb926f
ms.openlocfilehash: 624a375aedc78b6d63f3a6c5a1185edfade28c7d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97336144"
---
# <a name="compiler-error-c2761"></a>Ошибка компилятора C2761

"функция": повторное объявление функции члена не разрешено

Нельзя повторно объявить функцию-член. Его можно определить, но не объявлять повторно.

## <a name="examples"></a>Примеры

Следующий пример приводит к возникновению ошибки C2761.

```cpp
// C2761.cpp
class a {
   int t;
   void test();
};

void a::a;     // C2761
void a::test;  // C2761
```

Невозможно определить нестатические члены класса или структуры.  Следующий пример приводит к возникновению ошибки C2761.

```cpp
// C2761_b.cpp
// compile with: /c
struct C {
   int s;
   static int t;
};

int C::s;   // C2761
int C::t;   // OK
```
