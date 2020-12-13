---
description: 'Дополнительные сведения о: Неустранимая ошибка C1094'
title: Неустранимая ошибка C1094
ms.date: 11/04/2016
f1_keywords:
- C1094
helpviewer_keywords:
- C1094
ms.assetid: 9e1193b2-cb95-44f9-bf6f-019e0d41dd97
ms.openlocfilehash: af83c6fa80a6e1b115146ad05513539fea7d348c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97145097"
---
# <a name="fatal-error-c1094"></a>Неустранимая ошибка C1094

"-Zmval1": параметр командной строки не согласуется со значением, используемым для сборки предкомпилированного заголовка ("-Zmval2")

Значение, передаваемое в параметре [/Yc](../../build/reference/yc-create-precompiled-header-file.md) , должно иметь то же значение, которое передается в [/Yu](../../build/reference/yu-use-precompiled-header-file.md) (значения **/ZM** должны быть одинаковыми во всех компиляциях, использующих или создающих один и тот же предкомпилированный заголовочный файл).

Следующий пример приводит к возникновению ошибки C1094:

```
// C1094.h
int func1();
```

Затем:

```cpp
// C1094.cpp
// compile with: /Yc"C1094.h" /Zm200
int u;
int main() {
   int sd = 32;
}
#include "C1094.h"
```

Затем:

```cpp
// C1094b.cpp
// compile with: /Yu"C1094.h" /Zm300 /c
#include "C1094.h"   // C1094 compile with /Zm200
void Test() {}
```
