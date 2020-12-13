---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 4) C4670'
title: Предупреждение компилятора (уровень 4) C4670
ms.date: 11/04/2016
f1_keywords:
- C4670
helpviewer_keywords:
- C4670
ms.assetid: e172b134-b1fb-4dfe-8e9d-209ea08b73c7
ms.openlocfilehash: c1d0f81f10fe63882987d660e4b9099f4ff895ff
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97134034"
---
# <a name="compiler-warning-level-4-c4670"></a>Предупреждение компилятора (уровень 4) C4670

"идентификатор": этот базовый класс недоступен

Указанный базовый класс объекта, который должен быть создан в **`try`** блоке, недоступен. Если объект возник, то его экземпляры создавать нельзя. Обратите внимание, что базовый класс наследуется вместе с правильным спецификатором доступа.

Следующий пример приводит к возникновению предупреждения C4670:

```cpp
// C4670.cpp
// compile with: /EHsc /W4
class A
{
};

class B : /* public */ A
{
} b;   // inherits A with private access by default

int main()
{
    try
    {
       throw b;   // C4670
    }
    catch( B )
    {
    }
}
```
