---
description: 'Дополнительные сведения о: Ошибка компилятора C3155'
title: Ошибка компилятора C3155
ms.date: 11/04/2016
f1_keywords:
- C3155
helpviewer_keywords:
- C3155
ms.assetid: b04a42e1-64e7-40f8-81fe-c7945348b2cf
ms.openlocfilehash: 92fdf24c067c26502f8d24923e7f2c77b16c7922
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97242461"
---
# <a name="compiler-error-c3155"></a>Ошибка компилятора C3155

Использование атрибутов в индексаторе свойств не допускается

Индексированное свойство было объявлено неправильно. Дополнительные сведения см. в разделе [инструкции. Использование свойств в C++/CLI](../../dotnet/how-to-use-properties-in-cpp-cli.md).

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3155.

```cpp
// C3155.cpp
// compile with: /clr /c
using namespace System;
ref struct R {
   property int F[[ParamArray] int] {   // C3155
   // try the following line instead
   // property int F[ int] {   // OK
      int get(int i) {
         return 0;
      }
   }
};
```
