---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 3) C4290'
title: Предупреждение компилятора (уровень 3) C4290
ms.date: 11/04/2016
f1_keywords:
- C4290
helpviewer_keywords:
- C4290
ms.assetid: d1c6d85b-28e0-4a1f-9d48-23593337a6fb
ms.openlocfilehash: 771eb01c23778a716aee22ca747ea6473909a8bc
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97344072"
---
# <a name="compiler-warning-level-3-c4290"></a>Предупреждение компилятора (уровень 3) C4290

Спецификация исключения C++ игнорируется, кроме указания, что функция не __declspec (throw)

Функция объявляется с помощью спецификации исключения, которая Visual C++ принимает, но не реализует. Код с спецификациями исключений, которые игнорируются во время компиляции, может потребоваться перекомпилировать и связать с ними для повторного использования в будущих версиях, поддерживающих спецификации исключений.

Дополнительные сведения см. в разделе [спецификации исключений (throw)](../../cpp/exception-specifications-throw-cpp.md) .

Это предупреждение можно избежать с помощью директивы pragma [warning](../../preprocessor/warning.md) :

```cpp
#pragma warning( disable : 4290 )
```

Следующий пример кода приводит к возникновению ошибки C4290:

```cpp
// C4290.cpp
// compile with: /EHs /W3 /c
void f1(void) throw(int) {}   // C4290

// OK
void f2(void) throw() {}
void f3(void) throw(...) {}
```
