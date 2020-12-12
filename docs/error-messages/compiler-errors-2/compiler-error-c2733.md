---
description: 'Дополнительные сведения о: Ошибка компилятора C2733'
title: Ошибка компилятора C2733
ms.date: 11/04/2016
f1_keywords:
- C2733
helpviewer_keywords:
- C2733
ms.assetid: 67f83561-c633-407c-a2ee-f9fd16e165bf
ms.openlocfilehash: f957be13b8c1de1ee3ada98ffd42f0d89fc7755c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97123205"
---
# <a name="compiler-error-c2733"></a>Ошибка компилятора C2733

Вторая C компоновка перегруженной функции "функция" запрещена

С компоновкой C объявлено более одной перегруженной функции. При использовании компоновки C только одна форма указанной функции может быть внешней. Так как перегруженные функции имеют одно и то же недекорированное имя, их нельзя использовать с программами на языке C.

Следующий пример приводит к возникновению ошибки C2733:

```cpp
// C2733.cpp
extern "C" {
   void F1(int);
}

extern "C" {
   void F1();   // C2733
   // try the following line instead
   // void F2();
}
```
