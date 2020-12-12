---
description: 'Дополнительные сведения о: Ошибка компилятора C3836'
title: Ошибка компилятора C3836
ms.date: 11/04/2016
f1_keywords:
- C3836
helpviewer_keywords:
- C3836
ms.assetid: 254f851b-7b7d-4c34-a740-fcf72f6a636a
ms.openlocfilehash: c7e05bbf95facf5b8552b4442138cc38b86703c0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97180881"
---
# <a name="compiler-error-c3836"></a>Ошибка компилятора C3836

статический конструктор не может иметь список инициализаторов членов

Управляемый класс не может иметь статический конструктор, который также содержит список инициализации членов. Статические конструкторы классов вызываются средой CLR для инициализации класса, инициализации статических элементов данных.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3836:

```cpp
// C3836a.cpp
// compile with: /clr
ref class M
{
   static int s_i;

public:
   static M() :  s_i(1234)   // C3836, delete initializer to resolve
   {
   }
};

int main()
{
}
```
