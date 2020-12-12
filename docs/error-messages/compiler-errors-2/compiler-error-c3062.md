---
description: 'Дополнительные сведения о: Ошибка компилятора C3062'
title: Ошибка компилятора C3062
ms.date: 11/04/2016
f1_keywords:
- C3062
helpviewer_keywords:
- C3062
ms.assetid: 78632e6d-255f-42c3-b124-31a9194ff86d
ms.openlocfilehash: b57d03f3ef09e1d01741866d99dfff87aa5aa28d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97281747"
---
# <a name="compiler-error-c3062"></a>Ошибка компилятора C3062

"enum": для перечислителя требуется значение, так как базовый тип — "тип"

Для перечисления можно указать базовый тип. Однако для некоторых типов требуется назначить значения каждому перечислителю.

Дополнительные сведения о перечислениях см. в разделе [Класс Enum](../../extensions/enum-class-cpp-component-extensions.md).

Следующий пример приводит к возникновению ошибки C3062:

```cpp
// C3062.cpp
// compile with: /clr

enum class MyEnum : bool { a };   // C3062
enum class MyEnum2 : bool { a = true};   // OK
```
