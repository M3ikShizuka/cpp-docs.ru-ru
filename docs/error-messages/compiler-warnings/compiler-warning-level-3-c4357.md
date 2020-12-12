---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 3) C4357'
title: Предупреждение компилятора (уровень 3) C4357
ms.date: 11/04/2016
f1_keywords:
- C4357
helpviewer_keywords:
- C4357
ms.assetid: 9259c633-3c02-4900-b94a-2d8d366d61cd
ms.openlocfilehash: 89446d131d62134c181c691d8103f75b8cdbe4a4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97274246"
---
# <a name="compiler-warning-level-3-c4357"></a>Предупреждение компилятора (уровень 3) C4357

аргумент массива параметров в списке формальных аргументов для делегата "Del" игнорируется при создании "функция"

`ParamArray`Атрибут был проигнорирован и `function` не может быть вызван с переменными аргументами.

Следующий пример приводит к возникновению ошибки C4357:

```cpp
// C4357.cpp
// compile with: /clr /W3 /c
using namespace System;
public delegate void f(int i, ... array<Object^>^ varargs);   // C4357

public delegate void g(int i, array<Object^>^ varargs);   // OK
```
