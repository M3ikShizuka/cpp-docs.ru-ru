---
description: 'Дополнительные сведения о: Ошибка компилятора C3200'
title: Ошибка компилятора C3200
ms.date: 11/04/2016
f1_keywords:
- C3200
helpviewer_keywords:
- C3200
ms.assetid: 44bb5e77-f0ec-421c-a732-b9ee7c0a3529
ms.openlocfilehash: c693878628ff0bd9dddcb2f100ca652910b0fb89
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97330657"
---
# <a name="compiler-error-c3200"></a>Ошибка компилятора C3200

"шаблон": недопустимый аргумент шаблона для параметра шаблона "параметр", требуется шаблон класса

Передан недопустимый аргумент в шаблон класса. Шаблон класса принимает шаблон в качестве параметра. В следующем примере вызов `Y<int, int> aY` создаст C3200. Первый параметр должен быть шаблоном, например `Y<X, int> aY` .

```cpp
// C3200.cpp
template<typename T>
class X
{
};

template<template<typename U> class T1, typename T2>
class Y
{
};

int main()
{
   Y<int, int> y;   // C3200
}
```
