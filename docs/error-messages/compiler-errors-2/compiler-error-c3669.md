---
description: 'Дополнительные сведения о: Ошибка компилятора C3669'
title: Ошибка компилятора C3669
ms.date: 11/04/2016
f1_keywords:
- C3669
helpviewer_keywords:
- C3669
ms.assetid: be9c7ae4-e96f-47ab-922a-39a3537d5ca6
ms.openlocfilehash: b746c64af06178caf1006417f61c5f1e853cb67d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97228954"
---
# <a name="compiler-error-c3669"></a>Ошибка компилятора C3669

"член": спецификатор переопределения "override" не допускается в статических функциях или конструкторах членов

Переопределение указано неправильно. Дополнительные сведения см. в разделе [явные переопределения](../../extensions/explicit-overrides-cpp-component-extensions.md).

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3669.

```cpp
// C3669.cpp
// compile with: /clr
public ref struct R {
   R() override {}   // C3669
};
```
