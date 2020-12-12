---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 4) C4408'
title: Предупреждение компилятора (уровень 4) C4408
ms.date: 11/04/2016
f1_keywords:
- C4408
helpviewer_keywords:
- C4408
ms.assetid: 8488a186-ed1d-425c-aaeb-c72472c1da68
ms.openlocfilehash: 94764cd23c8bf4af757afa7bd8a084f61c5f24a0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97251483"
---
# <a name="compiler-warning-level-4-c4408"></a>Предупреждение компилятора (уровень 4) C4408

анонимаусструкт или Union не объявили элементы данных

У анонимной структуры или объединения должен быть по крайней мере один элемент данных.

Следующий пример приводит к возникновению ошибки C4408.

```cpp
// C4408.cpp
// compile with: /W4 /LD
static union
{
   // int i;
};
// a named union can have no data members
// } MyUnion;
```
