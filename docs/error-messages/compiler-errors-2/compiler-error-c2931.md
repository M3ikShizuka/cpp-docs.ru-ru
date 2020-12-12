---
description: 'Дополнительные сведения о: Ошибка компилятора C2931'
title: Ошибка компилятора C2931
ms.date: 11/04/2016
f1_keywords:
- C2931
helpviewer_keywords:
- C2931
ms.assetid: 33430407-b149-4ba3-baf8-b0dae1ea3a5d
ms.openlocfilehash: a4d659a0529fa80affc6749d150b9a567d015d90
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97320335"
---
# <a name="compiler-error-c2931"></a>Ошибка компилятора C2931

"класс": идентификатор класса типа переопределен как функция-член в "идентификатор"

Универсальный класс или класс-шаблон нельзя использовать в качестве функции-члена другого класса.

Эта ошибка может возникнуть при неправильной расстановке скобок.

Следующий пример приводит к возникновению ошибки C2931:

```cpp
// C2931.cpp
// compile with: /c
template<class T>
struct TC { };
struct MyStruct {
   void TC<int>();   // C2931
};

struct TC2 { };
struct MyStruct2 {
   void TC2();
};
```

Ошибка C2931 также может возникнуть при использовании универсальных шаблонов.

```cpp
// C2931b.cpp
// compile with: /clr /c
generic<class T> ref struct GC {};
struct MyStruct {
   void GC<int>();   // C2931
   void GC2();   // OK
};
```
