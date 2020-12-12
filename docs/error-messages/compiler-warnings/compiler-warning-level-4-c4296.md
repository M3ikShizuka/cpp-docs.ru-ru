---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 4) C4296'
title: Предупреждение компилятора (уровень 4) C4296
ms.date: 11/04/2016
f1_keywords:
- C4296
helpviewer_keywords:
- C4296
ms.assetid: 9d99aafe-f6bd-4ee0-b8d0-98ce5712274d
ms.openlocfilehash: 995c332a0f1ee46c9df7081dd34a97b51de40ac6
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97294539"
---
# <a name="compiler-warning-level-4-c4296"></a>Предупреждение компилятора (уровень 4) C4296

"оператор": выражение всегда имеет значение false

В операции сравнения с нулевым значением использовалась неподписанная переменная.

Это предупреждение отключено по умолчанию. Подробнее: [Выключенные по умолчанию предупреждения компилятора](../../preprocessor/compiler-warnings-that-are-off-by-default.md) .

Следующий пример приводит к возникновению ошибки C4296:

```cpp
// C4296.cpp
// compile with: /W4
#pragma warning(default : 4296)
int main()
{
   unsigned int u = 9;
   if (u < 0)    // C4296
      u++;
   if (u >= 0)   // C4296
      u++;
}
```
