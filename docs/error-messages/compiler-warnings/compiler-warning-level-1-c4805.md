---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4805'
title: Предупреждение компилятора (уровень 1) C4805
ms.date: 11/04/2016
f1_keywords:
- C4805
helpviewer_keywords:
- C4805
ms.assetid: 99c7b7e2-272e-4ab5-8580-17c42e62e2ef
ms.openlocfilehash: c63b117e20e6e4aef650ac07ba0475060cc37d0f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97238262"
---
# <a name="compiler-warning-level-1-c4805"></a>Предупреждение компилятора (уровень 1) C4805

"операция": небезопасное смешение типа "тип" и типа "тип" в операции

Это предупреждение создается для операций сравнения между [bool](../../cpp/bool-cpp.md) и [int](../../c-language/integer-types.md). Следующий пример приводит к возникновению ошибки C4805:

```cpp
// C4805.cpp
// compile with: /W1
int main() {
   int i = 1;
   bool b = true;

   if (i == b) {   // C4805, comparing bool and int variables
   }
}
```
