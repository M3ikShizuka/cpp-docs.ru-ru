---
description: 'Дополнительные сведения о: Ошибка компилятора C3292'
title: Ошибка компилятора C3292
ms.date: 11/04/2016
f1_keywords:
- C3292
helpviewer_keywords:
- C3292
ms.assetid: ead485cc-5471-4e10-b361-300589ff5b70
ms.openlocfilehash: 5c20ae5a03fd6eab442384c91c3357c2d9edb214
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97144694"
---
# <a name="compiler-error-c3292"></a>Ошибка компилятора C3292

пространство имен CLI нельзя открыть повторно

Пространство имен cli не может быть объявлено в вашем коде.  Дополнительные сведения см. в статье [Platform, default, and cli Namespaces (C++/CLI and C++/CX)](../../extensions/platform-default-and-cli-namespaces-cpp-component-extensions.md) (Пространства имен Platform, default и cli (C++/CLI и C++/CX)).

## <a name="example"></a>Пример

В следующем примере возникает ошибка C3292.

```cpp
// C3292.cpp
// compile with: /clr /c
namespace cli {};   // C3292
```
