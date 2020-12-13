---
description: 'Дополнительные сведения о: Ошибка компилятора C2457'
title: Ошибка компилятора C2457
ms.date: 11/04/2016
f1_keywords:
- C2457
helpviewer_keywords:
- C2457
ms.assetid: 347e169d-23ad-434f-8836-5b09b53980ff
ms.openlocfilehash: 1fea5192b97e280a38f674a67b0bf739041ffe97
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97332373"
---
# <a name="compiler-error-c2457"></a>Ошибка компилятора C2457

> "*макрос*": предопределенный макрос не может находиться за пределами тела функции

Предпринята попытка использования предопределенного макроса, например [&#95;&#95;функции&#95;&#95;](../../preprocessor/predefined-macros.md), в глобальном пространстве.

## <a name="example"></a>Пример

В следующем примере показано создание C2457, а также правильное использование:

```cpp
// C2457.cpp
#include <stdio.h>

__FUNCTION__;   // C2457, cannot be global

int main()
{
    printf_s("\n%s", __FUNCTION__);   // OK
}
```
