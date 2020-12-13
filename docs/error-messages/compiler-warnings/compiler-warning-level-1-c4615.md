---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4615'
title: Предупреждение компилятора (уровень 1) C4615
ms.date: 11/04/2016
f1_keywords:
- C4615
helpviewer_keywords:
- C4615
ms.assetid: 7b107c01-0da2-4e01-8b40-93813e30b94c
ms.openlocfilehash: 174ffa81e9f5927833b877ede7cf24ae530b94fb
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97339211"
---
# <a name="compiler-warning-level-1-c4615"></a>Предупреждение компилятора (уровень 1) C4615

\#pragma warning: неизвестный тип предупреждения пользователя

В [предупреждении](../../preprocessor/warning.md) **pragma** использован недопустимый спецификатор предупреждения. Чтобы устранить эту ошибку, используйте допустимый спецификатор предупреждения.

Следующий пример приводит к возникновению ошибки C4615:

```cpp
// C4615.cpp
// compile with: /W1 /LD
#pragma warning(enable : 4401)   // C4615, 'enable' not valid specifier

// use the code below to resolve the error
// #pragma warning(default : 4401)
```
