---
description: 'Дополнительные сведения о: Ошибка компилятора C2935'
title: Ошибка компилятора C2935
ms.date: 11/04/2016
f1_keywords:
- C2935
helpviewer_keywords:
- C2935
ms.assetid: e11ef90d-0756-4e43-8a09-4974c6aa72a3
ms.openlocfilehash: 853c1e51444454ffdbd09e8387d47eb9770d7fa7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97320309"
---
# <a name="compiler-error-c2935"></a>Ошибка компилятора C2935

"класс": идентификатор класса типа переопределен как глобальная функция

Универсальный класс или класс-шаблон нельзя использовать в качестве глобальной функции.

Эта ошибка может возникнуть при неправильной расстановке скобок.

Следующий пример приводит к возникновению ошибки C2935:

```cpp
// C2935.cpp
// compile with: /c
template<class T>
struct TC {};
void TC<int>() {}   // C2935

// OK
struct TC2 {};
void TC2() {}
```

Ошибка C2935 также может возникнуть при использовании универсальных шаблонов:

```cpp
// C2935b.cpp
// compile with: /clr /c
generic<class T>
ref struct GC { };
void GC<int>() {}   // C2935
void GC() {}   // OK
```
