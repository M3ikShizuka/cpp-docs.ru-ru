---
description: 'Дополнительные сведения о: Ошибка компилятора C2493'
title: Ошибка компилятора C2493
ms.date: 11/04/2016
f1_keywords:
- C2493
helpviewer_keywords:
- C2493
ms.assetid: 68316cd5-682b-49c3-b6ea-23c4e5d296cf
ms.openlocfilehash: 5b9f98fc2f21eadedd8316e60b249a387a0e80dc
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97283681"
---
# <a name="compiler-error-c2493"></a>Ошибка компилятора C2493

недопустимая форма __based

**`__based`** Выражение должно быть основано на указателе.

Следующий пример приводит к возникновению ошибки C2493:

```cpp
// C2493.cpp
// compile with: /c
char mybase;
int __based(mybase) ptr;   // C2493

// OK
char * mybase;
int __based(mybase) * ptr;
```
