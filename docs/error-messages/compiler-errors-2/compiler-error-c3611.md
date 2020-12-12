---
description: 'Дополнительные сведения о: Ошибка компилятора C3611'
title: Ошибка компилятора C3611
ms.date: 11/04/2016
f1_keywords:
- C3611
helpviewer_keywords:
- C3611
ms.assetid: 42f3e320-41de-420a-bd05-8924cab765aa
ms.openlocfilehash: 9c18e8e757e3962af1f2e0fbcc0d33384f3b6329
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97262299"
---
# <a name="compiler-error-c3611"></a>Ошибка компилятора C3611

"функция": запечатанная функция не может иметь чистый спецификатор

Запечатанная функция была объявлена неправильно.  Дополнительные сведения см. в статье [sealed (C++/CLI and C++/CX)](../../extensions/sealed-cpp-component-extensions.md).

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3611.

```cpp
// C3611.cpp
// compile with: /clr /c

ref struct V {
   virtual void Test() sealed = 0;   // C3611
   virtual void Test2() sealed;   // OK
   virtual void Test3() = 0;   // OK
};
```
