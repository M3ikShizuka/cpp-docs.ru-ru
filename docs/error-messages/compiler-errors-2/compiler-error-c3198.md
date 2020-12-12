---
description: 'Дополнительные сведения о: Ошибка компилятора C3198'
title: Ошибка компилятора C3198
ms.date: 11/04/2016
f1_keywords:
- C3198
helpviewer_keywords:
- C3198
ms.assetid: ec4ecf61-0067-4aa4-b443-a91013a1e59d
ms.openlocfilehash: 8f72dd32af7f004696afd87b7141768f09ea5f12
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97321987"
---
# <a name="compiler-error-c3198"></a>Ошибка компилятора C3198

Недопустимое использование директив pragma с плавающей запятой: fenv_access директива pragma работает только в точном режиме

Директива pragma [fenv_access](../../preprocessor/fenv-access.md) использовалась в параметре [/FP](../../build/reference/fp-specify-floating-point-behavior.md) , отличном от **/FP: точных**.

Следующий пример приводит к возникновению ошибки C3198:

```cpp
// C3198.cpp
// compile with: /fp:fast
#pragma fenv_access(on)   // C3198
```
