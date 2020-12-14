---
description: 'Дополнительные сведения о: Ошибка компилятора C3880'
title: Ошибка компилятора C3880
ms.date: 11/04/2016
f1_keywords:
- C3880
helpviewer_keywords:
- C3880
ms.assetid: b0e05d1e-32d0-4034-9246-f37d23573ea9
ms.openlocfilehash: c2d279cd50716f647fbbdf51f9f9c39863d4e2d2
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97274597"
---
# <a name="compiler-error-c3880"></a>Ошибка компилятора C3880

var: не может быть литеральным элементом данных

Тип [литерального](../../extensions/literal-cpp-component-extensions.md) атрибута должен быть или преобразован во время компиляции в один из следующих типов:

- целочисленный тип

- строка

- перечисление с целочисленным или базовым типом

Следующий пример приводит к возникновению ошибки C3880:

```cpp
// C3880.cpp
// compile with: /clr /c
ref struct Y1 {
   literal System::Decimal staticConst1 = 10;   // C3880
   literal int staticConst2 = 10;   // OK
};
```
