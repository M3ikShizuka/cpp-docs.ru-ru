---
description: 'Дополнительные сведения о: Ошибка компилятора C2177'
title: Ошибка компилятора C2177
ms.date: 11/04/2016
f1_keywords:
- C2177
helpviewer_keywords:
- C2177
ms.assetid: 2a39a880-cddb-4d3e-a572-645a14c4c478
ms.openlocfilehash: d03e227b98d13c097c47843fc99f0850372286c2
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97322140"
---
# <a name="compiler-error-c2177"></a>Ошибка компилятора C2177

слишком большая константа

Значение константы слишком велико для типа переменной, которой оно назначено.

В следующем примере возникает ошибка C2177:

```cpp
// C2177.cpp
int main() {
   int a=18446744073709551616;   // C2177
   int b=18446744073709551615;   // OK
}
```
