---
description: 'Дополнительные сведения о: Ошибка компилятора C2710'
title: Ошибка компилятора C2710
ms.date: 11/04/2016
f1_keywords:
- C2710
helpviewer_keywords:
- C2710
ms.assetid: a2a6bb5b-86ad-4a6c-acd0-e2bef8464e0e
ms.openlocfilehash: ea9e4eaefa023362647f418be16a72ee14fbd044
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97320861"
---
# <a name="compiler-error-c2710"></a>Ошибка компилятора C2710

"конструкция": "__declspec (модификатор)" может применяться только к функции, возвращающей указатель

Функция, возвращаемое значение которой является указателем, является единственной конструкцией, к которой `modifier` можно применить.

Следующий пример приводит к возникновению ошибки C2710:

```cpp
// C2710.cpp
__declspec(restrict) void f();   // C2710
// try the following line instead
__declspec(restrict) int * g();
```
