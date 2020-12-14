---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4835'
title: Предупреждение компилятора (уровень 1) C4835
ms.date: 11/04/2016
f1_keywords:
- C4835
helpviewer_keywords:
- C4835
ms.assetid: d2e44c62-7b0e-4a45-943d-97903e27ed9d
ms.openlocfilehash: ee5d91883bafcac3412962f7e314f2ee00ea8278
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97197989"
---
# <a name="compiler-warning-level-1-c4835"></a>Предупреждение компилятора (уровень 1) C4835

"переменная": инициализатор экспортируемых данных не будет выполняться до первого выполнения управляемого кода в сборке узла

При доступе к данным между управляемыми компонентами рекомендуется не использовать собственные механизмы импорта и экспорта C++. Вместо этого объявите элементы данных внутри управляемого типа и соберите ссылки на метаданные `#using` в клиенте. Дополнительные сведения см. в разделе [Директива using](../../preprocessor/hash-using-directive-cpp.md).

## <a name="examples"></a>Примеры

Следующий пример приводит к возникновению ошибки C4835.

```cpp
// C4835.cpp
// compile with: /W1 /clr /LD
int f() { return 1; }
int n = 9;

__declspec(dllexport) int m = f();   // C4835
__declspec(dllexport) int *p = &n;   // C4835
```

В следующем примере используется компонент, встроенный в предыдущем примере, показывающий, что значения переменных не так, как ожидалось.

```cpp
// C4835_b.cpp
// compile with: /clr C4835.lib
#include <stdio.h>
__declspec(dllimport) int m;
__declspec(dllimport) int *p;

int main() {
   printf("%d\n", m);
   printf("%d\n", p);
}
```

```Output
0
268456008
```
