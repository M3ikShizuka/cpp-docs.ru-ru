---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4163'
title: Предупреждение компилятора (уровень 1) C4163
ms.date: 11/04/2016
f1_keywords:
- C4163
helpviewer_keywords:
- C4163
ms.assetid: b08413fd-03fc-4f41-9167-a98976ac12f2
ms.openlocfilehash: 6906b8c7926371a57ddcd6677d0c34ef57bbb383
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97267122"
---
# <a name="compiler-warning-level-1-c4163"></a>Предупреждение компилятора (уровень 1) C4163

"идентификатор": недоступен в качестве подставляемой функции

Указанная функция не может использоваться как [встроенная](../../preprocessor/intrinsic.md) функция. Компилятор игнорирует неправильное имя функции.

Следующий пример приводит к возникновению ошибки C4163.

```cpp
// C4163.cpp
// compile with: /W1 /LD
#include <math.h>
#pragma intrinsic(mysin)   // C4163
// try the following line instead
// #pragma intrinsic(sin)
```
