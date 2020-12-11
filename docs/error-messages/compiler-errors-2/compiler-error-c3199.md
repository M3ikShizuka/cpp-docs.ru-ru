---
description: 'Дополнительные сведения о: Ошибка компилятора C3199'
title: Ошибка компилятора C3199
ms.date: 11/04/2016
f1_keywords:
- C3199
helpviewer_keywords:
- C3199
ms.assetid: e7a478d3-115a-40a3-991b-c7454fd2e28e
ms.openlocfilehash: 598d21edbddc91d39edb9623dc59537d3e27bdf3
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97155479"
---
# <a name="compiler-error-c3199"></a>Ошибка компилятора C3199

Недопустимое использование директив pragma с плавающей запятой: исключения не поддерживаются в режиме без точности

Директива pragma [float_control](../../preprocessor/float-control.md) использовалась для указания модели исключения с плавающей запятой в параметре [/FP](../../build/reference/fp-specify-floating-point-behavior.md) , отличном от **/FP: точнее**.

Следующий пример приводит к возникновению ошибки C3199:

```cpp
// C3199.cpp
// compile with: /fp:fast
#pragma float_control(except, on)   // C3199
```
