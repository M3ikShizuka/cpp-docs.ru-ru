---
description: 'Дополнительные сведения о: Ошибка компилятора C3797'
title: Ошибка компилятора C3797
ms.date: 11/04/2016
f1_keywords:
- C3797
helpviewer_keywords:
- C3797
ms.assetid: ab27ff34-8c1d-4297-b004-9e39bd3a4f25
ms.openlocfilehash: 581dae7ba2649d72fc2670b99c9255b3ee9f7838
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97244866"
---
# <a name="compiler-error-c3797"></a>Ошибка компилятора C3797

"override": объявление события не может иметь спецификатор переопределения (следует размещать в методах Add/Remove/raise события)

Нельзя переопределить тривиальное событие (событие без явно определенных методов доступа) другим тривиальным событием. Переопределяющее событие должно определять его поведение с помощью функций доступа.

Дополнительные сведения см. в разделе [event](../../extensions/event-cpp-component-extensions.md).

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3797.

```cpp
// C3797.cpp
// compile with: /clr /c
delegate void MyDel();

ref class Class1 {
public:
   virtual event MyDel ^ E;
};

ref class Class2 : public Class1 {
public:
   virtual event MyDel ^ E override;   // C3797
};

// OK
ref class Class3 : public Class1 {
public:
   virtual event MyDel ^ E {
      void add(MyDel ^ d) override {}
      void remove(MyDel ^ d) override {}
   }
};
```
