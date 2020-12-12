---
description: 'Дополнительные сведения о: Ошибка компилятора C2448'
title: Ошибка компилятора C2448
ms.date: 11/04/2016
f1_keywords:
- C2448
helpviewer_keywords:
- C2448
ms.assetid: e255df3c-f861-4b4d-a193-8768cef061a5
ms.openlocfilehash: 8dc6f794a71c89b4b14d0a3f33d5617e296b3dc1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97189617"
---
# <a name="compiler-error-c2448"></a>Ошибка компилятора C2448

"идентификатор": вероятно, инициализатор в стиле функции является определением функции

Неверное определение функции.

Эта ошибка может быть вызвана официальным списком в старом стиле C-Language.

Следующий пример приводит к возникновению ошибки C2448:

```cpp
// C2448.cpp
void func(c)
   int c;
{}   // C2448
```
