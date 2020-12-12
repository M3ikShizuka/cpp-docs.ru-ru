---
description: 'Дополнительные сведения о: Ошибка компилятора C2134'
title: Ошибка компилятора C2134
ms.date: 11/04/2016
f1_keywords:
- C2134
ms.assetid: d45cb3e8-0be4-4bd6-8be9-5f8d2384363f
ms.openlocfilehash: 16149c3b3f28720670c26f0fae2a89d1b7b6f8b4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97323117"
---
# <a name="compiler-error-c2134"></a>Ошибка компилятора C2134

"функция": вызов не приводит к константному выражению

Функция, объявленная как constexpr, может вызывать только другие функции, объявленные как constexpr.

Следующий пример приводит к возникновению ошибки C2134:

```cpp
// C2134.cpp
// compile with: /c
int A() {
    return 42;
};

constexpr int B() {
    return A();  // Error C2134: 'A': call does not result in a constant expression.
}
```

Возможное решение:

```cpp
// C2134b.cpp
constexpr int A() {  // add constexpr to A, since it meets the requirements of constexpr.
    return 42;
};

constexpr int B() {
    return A();  // No error
}
```
