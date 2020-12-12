---
description: 'Дополнительные сведения: false (C++)'
title: false (C++)
ms.date: 11/04/2016
f1_keywords:
- false_cpp
helpviewer_keywords:
- false keyword [C++]
ms.assetid: cc13aec5-1f02-4d38-8dbf-5473ea2b354f
ms.openlocfilehash: 73f1f07c858f0a578cc2d3135e560cc8e0cb9d32
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97319460"
---
# <a name="false-c"></a>false (C++)

Ключевое слово является одним из двух значений для переменной типа [bool](../cpp/bool-cpp.md) или условного выражения (условное выражение теперь является **`true`** логическим выражением). Например, если `i` является переменной типа **`bool`** , `i = false;` оператор присваивает значение **`false`** `i` .

## <a name="example"></a>Пример

```cpp
// bool_false.cpp
#include <stdio.h>

int main()
{
    bool bb = true;
    printf_s("%d\n", bb);
    bb = false;
    printf_s("%d\n", bb);
}
```

```Output
1
0
```

## <a name="see-also"></a>См. также раздел

[Ключевые слова](../cpp/keywords-cpp.md)
