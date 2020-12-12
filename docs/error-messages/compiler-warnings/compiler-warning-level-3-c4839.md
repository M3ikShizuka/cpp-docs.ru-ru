---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 3) C4839'
title: Предупреждение компилятора (уровень 3) C4839
ms.date: 09/13/2018
f1_keywords:
- C4839
helpviewer_keywords:
- C4839
ms.assetid: f4f99066-9258-4330-81a8-f4a75a1d95ee
ms.openlocfilehash: a8ae0d3e3c74c62d05163edd981679e5390fb184
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97332069"
---
# <a name="compiler-warning-level-3-c4839"></a>Предупреждение компилятора (уровень 3) C4839

> нестандартное использование класса "*Type*" в качестве аргумента функции Variadic

Классы или структуры, которые передаются в функцию Variadic, например, `printf` должны быть простыми копируемыми. При передаче таких объектов компилятор просто выполняет побитовое копирование и не вызывает конструктор или деструктор.

Это предупреждение доступно начиная с Visual Studio 2017.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C4839:

```cpp
// C4839.cpp
// compile by using: cl /EHsc /W3 C4839.cpp
#include <atomic>
#include <memory>
#include <stdio.h>

int main()
{
    std::atomic<int> i(0);
    printf("%i\n", i); // error C4839: non-standard use of class 'std::atomic<int>'
                        // as an argument to a variadic function
                        // note: the constructor and destructor will not be called;
                        // a bitwise copy of the class will be passed as the argument
                        // error C2280: 'std::atomic<int>::atomic(const std::atomic<int> &)':
                        // attempting to reference a deleted function
}
```

Чтобы исправить эту ошибку, можно вызвать функцию-член, возвращающую тип, доступный для простого копирования,

```cpp
    std::atomic<int> i(0);
    printf("%i\n", i.load());
```

Для строк, созданных и управляемых с помощью `CStringW`, следует использовать предоставленный `operator LPCWSTR()` для приведения объекта `CStringW` к указателю C, ожидаемому строкой формата.

```cpp
    CStringW str1;
    CStringW str2;
    // ...
    str1.Format("%s", static_cast<LPCWSTR>(str2));
```
