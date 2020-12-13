---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4145'
title: Предупреждение компилятора (уровень 1) C4145
ms.date: 11/04/2016
f1_keywords:
- C4145
helpviewer_keywords:
- C4145
ms.assetid: 0440777a-cca2-4159-aff5-e67a254ad64a
ms.openlocfilehash: 2eaafd131e7dcfba7b94fbc84e5c2b9da2dfa89e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97136257"
---
# <a name="compiler-warning-level-1-c4145"></a>Предупреждение компилятора (уровень 1) C4145

"выражение1": использование выражения с оператором отношения в качестве выражения для выбора вариантов; возможное смешение с "выражение2"

**`switch`** Оператор использует реляционное выражение в качестве выражения элемента управления, что приводит к логическому значению для **`case`** инструкций. Вы имели в виду *выражение2*?

## <a name="example"></a>Пример

При компиляции следующего примера будет выдано предупреждение C4145:

```cpp
// C4145.cpp
// compile with: /W1
int main() {
   int i = 0;
   switch(i == 1) {   // C4145, use i instead of i == 1 to resolve
      case 1:
         break;
      default:
         break;
   }
}
```
