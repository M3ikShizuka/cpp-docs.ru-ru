---
description: 'Дополнительные сведения о: Ошибка компилятора C2995'
title: Ошибка компилятора C2995
ms.date: 11/04/2016
f1_keywords:
- C2995
helpviewer_keywords:
- C2995
ms.assetid: a57cdfe0-b40b-4a67-a95c-1a49ace4842b
ms.openlocfilehash: af78382ea11cda0ba33dc398c2983c65e31b653d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97253706"
---
# <a name="compiler-error-c2995"></a>Ошибка компилятора C2995

"функция": шаблон функции уже определен

Убедитесь в том, что для каждой функции-члена шаблонного класса существует только одно определение.

Следующий пример приводит к возникновению ошибки C2995:

```cpp
// C2995.cpp
// compile with: /c
template <class T>
void Test(T x){}

template <class T> void Test(T x){}   // C2995
template <class T> void Test2(T x){}   // OK
```
