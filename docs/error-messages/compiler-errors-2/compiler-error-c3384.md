---
description: 'Дополнительные сведения о: Ошибка компилятора C3384'
title: Ошибка компилятора C3384
ms.date: 11/04/2016
f1_keywords:
- C3384
helpviewer_keywords:
- C3384
ms.assetid: c9f92c6a-62a9-4333-b2b1-bc55c7f288b6
ms.openlocfilehash: 79d5aabf185702c3d85485744b14e714a32aa76b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97285582"
---
# <a name="compiler-error-c3384"></a>Ошибка компилятора C3384

"параметр_типа": ограничение значения и ссылочное ограничение взаимно исключают друг друга

Универсальный тип нельзя ограничить как для, так **`value class`** и для **`ref class`** .

Дополнительные сведения см. [в разделе ограничения для параметров универсального типа (C++/CLI)](../../extensions/constraints-on-generic-type-parameters-cpp-cli.md) .

## <a name="example"></a>Пример

При компиляции следующего примера возникнет ошибка C3384.

```cpp
// C3384.cpp
// compile with: /c /clr
generic <typename T>
where T : ref class
where T : value class   // C3384
ref class List {};
```
