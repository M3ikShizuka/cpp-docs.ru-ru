---
description: 'Дополнительные сведения о: Ошибка компилятора C2004'
title: Ошибка компилятора C2004
ms.date: 11/04/2016
f1_keywords:
- C2004
helpviewer_keywords:
- C2004
ms.assetid: d81526dd-3a00-4593-87b0-d910d3d29bca
ms.openlocfilehash: f418d2c2c372b228cc50b82237d8ebc56321e2c7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97340389"
---
# <a name="compiler-error-c2004"></a>Ошибка компилятора C2004

требуется "defined(id)"

Идентификатор должен быть заключен в круглые скобки после ключевого слова препроцессора.

Эта ошибка также может возникать в результате действий по обеспечению совместимости компилятора с Visual Studio .NET 2003: отсутствуют круглые скобки в директиве препроцессора. Если в директиве препроцессора отсутствует закрывающая круглая скобка, компилятор выдаст сообщение об ошибке.

## <a name="examples"></a>Примеры

Следующий пример приводит к возникновению ошибки C2004:

```cpp
// C2004.cpp
// compile with: /DDEBUG
#include <stdio.h>

int main()
{
    #if defined(DEBUG   // C2004
        printf_s("DEBUG defined\n");
    #endif
}
```

Возможное решение:

```cpp
// C2004b.cpp
// compile with: /DDEBUG
#include <stdio.h>

int main()
{
    #if defined(DEBUG)
        printf_s("DEBUG defined\n");
    #endif
}
```
