---
description: 'Дополнительные сведения о: предупреждение компилятора C4693'
title: Предупреждение компилятора C4693
ms.date: 10/25/2017
f1_keywords:
- C4693
helpviewer_keywords:
- C4693
ms.assetid: 72d8db01-5e6f-4794-8731-76107e8f064a
ms.openlocfilehash: 114809e1f73eb3d4e3481f0baa348d5eb478f4f1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97315105"
---
# <a name="compiler-warning-c4693"></a>Предупреждение компилятора C4693

> "класс": у запечатанного абстрактного класса не может быть членов экземпляра "Тест"

Если тип помечен как [sealed](../../extensions/sealed-cpp-component-extensions.md) и [abstract](../../extensions/abstract-cpp-component-extensions.md), он может иметь только статические члены.

Это предупреждение автоматически повышается до ошибки. Если вы хотите изменить это поведение, используйте [#pragma предупреждение](../../preprocessor/warning.md).

## <a name="example"></a>Пример

Следующий пример приводит к возникновению предупреждения C4693:

```cpp
// C4693.cpp
// compile with: /clr /c
public ref class Public_Ref_Class sealed abstract {
public:
   void Test() {}   // C4693
   static void Test2() {}   // OK
};
```
