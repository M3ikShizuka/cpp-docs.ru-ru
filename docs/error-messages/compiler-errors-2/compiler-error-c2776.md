---
description: 'Дополнительные сведения о: Ошибка компилятора C2776'
title: Ошибка компилятора C2776
ms.date: 11/04/2016
f1_keywords:
- C2776
helpviewer_keywords:
- C2776
ms.assetid: 9d80addc-62c7-40fc-a2cc-60303abb87df
ms.openlocfilehash: 75e0121c61fd55aa89e6ffcc6e1ed00137fcaaca
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97298140"
---
# <a name="compiler-error-c2776"></a>Ошибка компилятора C2776

для свойства можно указать только один метод "Get"

`get`В расширенном атрибуте [Property](../../cpp/property-cpp.md) можно указать только одну функцию. Эта ошибка возникает, если `get` указано несколько функций.

Следующий пример приводит к возникновению ошибки C2776:

```cpp
// C2776.cpp
struct A {
   __declspec(property(get=GetProp,get=GetPropToo))
   // try the following line instead
   // __declspec(property(get=GetProp))
      int prop;   // C2776
   int GetProp(void);
   int GetPropToo(void);
};
```
