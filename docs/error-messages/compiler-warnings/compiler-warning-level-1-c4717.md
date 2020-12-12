---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4717'
title: Предупреждение компилятора (уровень 1) C4717
ms.date: 11/04/2016
f1_keywords:
- C4717
helpviewer_keywords:
- C4717
ms.assetid: 5ef3c6c7-8599-4714-a973-0f5b69cdab3c
ms.openlocfilehash: 7a23469539dd809ea4905701bd1f8064f26a8036
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97328132"
---
# <a name="compiler-warning-level-1-c4717"></a>Предупреждение компилятора (уровень 1) C4717

"функция": рекурсивно для всех путей управления, функция приведет к переполнению стека времени выполнения

Каждый путь через функцию содержит вызов функции. Поскольку нет способа выйти из функции без первого вызова самой себя, функция никогда не будет выходить.

Следующий пример приводит к возникновению ошибки C4717:

```cpp
// C4717.cpp
// compile with: /W1 /c
// C4717 expected
int func(int x) {
   if (x > 1)
      return func(x - 1); // recursive call
   else {
      int y = func(0) + 1; // recursive call
      return y;
   }
}

int main(){
   func(1);
}
```
