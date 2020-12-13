---
description: 'Дополнительные сведения о: Ошибка компилятора C2258'
title: Ошибка компилятора C2258
ms.date: 11/04/2016
f1_keywords:
- C2258
helpviewer_keywords:
- C2258
ms.assetid: 105eaa87-befb-4ecb-9a3f-e09e14d2f5bf
ms.openlocfilehash: cb82994b582df91198fcd7455179666e66543247
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97134723"
---
# <a name="compiler-error-c2258"></a>Ошибка компилятора C2258

недопустимый строгий синтаксис, требуется "= 0"

Чистая виртуальная функция объявлена с неправильным синтаксисом.

Следующий пример приводит к возникновению ошибки C2258:

```cpp
// C2258.cpp
// compile with: /c
class A {
public:
   void virtual func1() = 1; // C2258
   void virtual func2() = 0;   // OK
};
```
