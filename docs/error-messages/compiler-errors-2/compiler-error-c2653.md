---
description: 'Дополнительные сведения о: Ошибка компилятора C2653'
title: Ошибка компилятора C2653
ms.date: 11/30/2017
f1_keywords:
- C2653
helpviewer_keywords:
- C2653
ms.assetid: 3f49e731-affd-43a0-a8d0-181db7650bc3
ms.openlocfilehash: f3be7ade8a6dcfc6aa8c5a83cc8a055fc230789d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97286154"
---
# <a name="compiler-error-c2653"></a>Ошибка компилятора C2653

> "*идентификатор*": не является именем класса или пространства имен

Для синтаксиса языка требуется имя класса, структуры, объединения или пространства имен.

Эта ошибка может возникать при использовании имени, которое не было объявлено в качестве класса, структуры, объединения или пространства имен перед оператором SCOPE. Чтобы устранить эту проблему, объявите имя или включите заголовок, объявляющий имя перед использованием.

C2653 также возможно при попытке определить *составное пространство* имен, которое содержит одно или несколько имен вложенных пространств имен. Определения составных пространств имен не допускаются в C++ до C++ 17. Составные пространства имен поддерживаются начиная с Visual Studio 2015 с обновлением 3 при указании параметра компилятора [/std: c + + Latest](../../build/reference/std-specify-language-standard-version.md) . Начиная с Visual Studio 2017 версии 15,5 компилятор поддерживает определения составных пространств имен, если указан параметр [/std: c++ 17](../../build/reference/std-specify-language-standard-version.md) .

## <a name="examples"></a>Примеры

Этот пример создает C2653, так как имя области используется, но не объявлено. Компилятор принимает имя класса, структуры, объединения или пространства имен перед оператором SCOPE (::).

```cpp
// C2653.cpp
// compile with: /c
class yy {
   void func1(int i);
};

void xx::func1(int m) {}   // C2653, xx is not declared
void yy::func1(int m) {}   // OK
```

В коде, который не компилируется для стандартов C++ 17 или более поздних версий, вложенные пространства имен должны использовать явное объявление пространства имен на каждом уровне вложенности:

```cpp
// C2653b.cpp
namespace a::b {int i;}   // C2653 prior to Visual Studio 2015 Update 3,
                          // C2429 thereafter. Use /std:c++17 or /std:c++latest to fix.

namespace a {             // Use this form for compliant code under /std:c++14 (the default)
   namespace b {          // or when using compilers before Visual Studio 2015 update 3.
      int i;
   }
}

int main() {
   a::b::i = 2;
}
```
