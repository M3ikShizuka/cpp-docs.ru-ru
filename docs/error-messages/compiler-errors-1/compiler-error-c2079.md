---
description: 'Дополнительные сведения о: Ошибка компилятора C2079'
title: Ошибка компилятора C2079
ms.date: 11/04/2016
f1_keywords:
- C2079
helpviewer_keywords:
- C2079
ms.assetid: ca58d6d5-eccd-40b7-ba14-c003223c5bc7
ms.openlocfilehash: 73ca5d334ac3bf3157b61a1b2a9489282ae1fe00
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97151220"
---
# <a name="compiler-error-c2079"></a>Ошибка компилятора C2079

"идентификатор" использует неопределенный класс, структуру или объединение "имя"

Указанный идентификатор является неопределенным классом, структурой или объединением.

Эта ошибка может быть вызвана инициализацией анонимного объединения.

Следующий пример приводит к возникновению ошибки C2079:

```cpp
// C2079.cpp
// compile with: /EHsc
#include <iostream>
int main() {
   std::ifstream g;   // C2079
}
```

Возможное решение:

```cpp
// C2079b.cpp
// compile with: /EHsc
#include <fstream>
int main( ) {
   std::ifstream g;
}
```

C2079 также может возникать при попытке объявить объект в стеке типа, объявление прямого объявления которого находится только в области.

```cpp
// C2079c.cpp
class A;

class B {
   A a;   // C2079
};

class A {};
```

Возможное решение:

```cpp
// C2079d.cpp
// compile with: /c
class A;
class C {};

class B {
   A * a;
   C c;
};

class A {};
```
