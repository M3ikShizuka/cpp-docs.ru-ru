---
description: 'Дополнительные сведения о: Ошибка компилятора C2681'
title: Ошибка компилятора C2681
ms.date: 11/04/2016
f1_keywords:
- C2681
helpviewer_keywords:
- C2681
ms.assetid: eb42da6d-8d2c-43fd-986b-e73e2b004885
ms.openlocfilehash: 3b002e6260787e60377d726bcceb6db41fce532a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97267785"
---
# <a name="compiler-error-c2681"></a>Ошибка компилятора C2681

"тип": недопустимый тип выражения для имени

Оператор приведения попытался преобразовать из недопустимого типа. Например, если для преобразования выражения в тип указателя используется оператор [dynamic_cast](../../cpp/dynamic-cast-operator.md) , исходное выражение должно быть указателем.

Следующий пример приводит к возникновению ошибки C2681:

```cpp
// C2681.cpp
class A { virtual void f(); };

void g(int i) {
    A* pa;
    pa = dynamic_cast<A*>(i);  // C2681
}
```
