---
description: 'Дополнительные сведения о: Ошибка компилятора C3645'
title: Ошибка компилятора C3645
ms.date: 11/04/2016
f1_keywords:
- C3645
helpviewer_keywords:
- C3645
ms.assetid: 346da528-ae86-4cd0-9654-f41bee26ac0d
ms.openlocfilehash: 198b22b80a4975d8bd6fab130c075621f248a93c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97203774"
---
# <a name="compiler-error-c3645"></a>Ошибка компилятора C3645

"функция": __clrcall нельзя использовать для функций, скомпилированных в машинный код

Наличие некоторых ключевых слов в функции приведет к компиляции функции в машинный код.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3645.

```cpp
// C3645.cpp
// compile with: /clr /c
#pragma unmanaged
int __clrcall dog() {}   // C3645
```
