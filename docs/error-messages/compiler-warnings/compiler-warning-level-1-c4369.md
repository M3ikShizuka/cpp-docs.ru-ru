---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4369'
title: Предупреждение компилятора (уровень 1) C4369
ms.date: 11/04/2016
f1_keywords:
- C4369
helpviewer_keywords:
- C4369
ms.assetid: ade87e84-36be-4e00-be99-2930af848feb
ms.openlocfilehash: 97f7882438124e8788559ec1453bd84d3ec371d2
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97339973"
---
# <a name="compiler-warning-level-1-c4369"></a>Предупреждение компилятора (уровень 1) C4369

"Enumerator": значение перечислителя "значение" не может быть представлено как "тип", значение "new_value"

Перечислитель был вычислен так, чтобы быть больше максимального значения для указанного базового типа.  Это привело к переполнению, и компилятор оборачивает значение перечислителя на наименьшее возможное значение для типа.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C4369.

```cpp
// C4369.cpp
// compile with: /W1
int main() {
   enum Color: char { red = 0x7e, green, blue };   // C4369
   enum Color2: char { red2 = 0x7d, green2, blue2};   // OK
}
```
