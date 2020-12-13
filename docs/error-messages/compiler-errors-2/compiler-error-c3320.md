---
description: 'Дополнительные сведения о: Ошибка компилятора C3320'
title: Ошибка компилятора C3320
ms.date: 11/04/2016
f1_keywords:
- C3320
helpviewer_keywords:
- C3320
ms.assetid: 2ef72d9a-1f1d-4b2e-b244-9fd3f3e70cb6
ms.openlocfilehash: 2dde804792dec4f7a1564c680a45c78adf60eedf
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97337373"
---
# <a name="compiler-error-c3320"></a>Ошибка компилятора C3320

"тип": имя типа не может совпадать со свойством name модуля

Экспортированный определяемый пользователем тип (UDT), который может быть структурой, классом, перечислением или объединением, не может иметь то же имя, что и параметр, передаваемый свойству Name атрибута [module](../../windows/attributes/module-cpp.md) .

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3320:

```cpp
// C3320.cpp
#include "unknwn.h"
[module(name="xx")];

[export] struct xx {   // C3320
// Try the following line instead
// [export] struct yy {
   int i;
};
```
