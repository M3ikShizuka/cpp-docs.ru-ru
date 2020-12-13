---
description: 'Дополнительные сведения о: Ошибка компилятора C2233'
title: Ошибка компилятора C2233
ms.date: 11/04/2016
f1_keywords:
- C2233
helpviewer_keywords:
- C2233
ms.assetid: 236bdf0b-9607-4f26-a249-d8def0b1333c
ms.openlocfilehash: d111a20fa9cac5a41566f63f6e3eef0c14ef544c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97338778"
---
# <a name="compiler-error-c2233"></a>Ошибка компилятора C2233

"идентификатор": массивы объектов, содержащие массивы нулевого размера, недопустимы

Каждый объект в массиве должен содержать по крайней мере один элемент.

Следующий пример приводит к возникновению ошибки C2233:

```cpp
// C2233.cpp
// compile with: /c
class A {
   char somearray[1];
};

class B {
   char zeroarray[];
};

A array[100];   // OK
B array2[100];   // C2233
```
