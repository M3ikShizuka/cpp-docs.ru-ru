---
description: 'Дополнительные сведения о: Ошибка компилятора C2009'
title: Ошибка компилятора C2009
ms.date: 11/04/2016
f1_keywords:
- C2009
helpviewer_keywords:
- C2009
ms.assetid: fe9d94ed-20a5-4d83-b9c4-60ee69d2f30a
ms.openlocfilehash: e7cc3078a8e404635dda531533bd3b1c629a0155
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97221056"
---
# <a name="compiler-error-c2009"></a>Ошибка компилятора C2009

повторное использование формального параметра макроса "идентификатор"

Список формальных параметров в определении макроса использует идентификатор более одного раза. Идентификаторы в списке параметров макроса должны быть уникальными.

## <a name="examples"></a>Примеры

Следующий пример приводит к возникновению ошибки C2009:

```cpp
// C2009.cpp
#include <stdio.h>

#define macro1(a,a) (a*a)   // C2009

int main()
{
    printf_s("%d\n", macro1(2));
}
```

Возможное решение:

```cpp
// C2009b.cpp
#include <stdio.h>

#define macro2(a)   (a*a)
#define macro3(a,b) (a*b)

int main()
{
    printf_s("%d\n", macro2(2));
    printf_s("%d\n", macro3(2,4));
}
```
