---
description: 'Дополнительные сведения о: Ошибка компилятора C2287'
title: Ошибка компилятора C2287
ms.date: 11/04/2016
f1_keywords:
- C2287
helpviewer_keywords:
- C2287
ms.assetid: 64556299-4e1f-4437-88b7-2464fc0b95bb
ms.openlocfilehash: 00a99ee553b4afc86a49ce80c61f2733c70b716f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97124050"
---
# <a name="compiler-error-c2287"></a>Ошибка компилятора C2287

"класс": представление наследования: "representation1" является менее общим, чем обязательный "representation2"

Класс объявлен с более простым представлением, чем требуется.

Следующий пример приводит к возникновению ошибки C2287:

```cpp
// C2287.cpp
// compile with: /vmg /c
class __single_inheritance X;
class __single_inheritance Y;

struct A { };
struct B { };
struct X : A, B { };  // C2287  X uses multiple inheritance
struct Y : A { };  // OK
```
