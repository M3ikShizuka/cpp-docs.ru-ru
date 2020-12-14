---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1 и уровень 4) C4700'
title: Предупреждение компилятора (уровень 1 и уровень 4) C4700
ms.date: 02/21/2018
f1_keywords:
- C4700
helpviewer_keywords:
- C4700
ms.assetid: 2da0deb4-77dd-4b05-98d3-b78d74ac4ca7
ms.openlocfilehash: 7ba19bdd6d8e25e095f796adc8cdb60b5cc8d325
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97241603"
---
# <a name="compiler-warning-level-1-and-level-4-c4700"></a>Предупреждение компилятора (уровень 1 и уровень 4) C4700

> использована неинициализированная локальная переменная "*имя*"

Было *использовано* локальное *имя* переменной, т. е. чтение из, прежде чем ему будет присвоено значение. В C и C++ локальные переменные не инициализируются по умолчанию. Неинициализированные переменные могут содержать любое значение, и их использование приводит к неопределенному поведению. Предупреждение C4700 почти всегда указывает на ошибку, которая может привести к непредсказуемым результатам или сбоям в программе.

Чтобы устранить эту проблему, можно инициализировать локальные переменные при их объявлении или присвоить им значения до их использования. Функцию можно использовать для инициализации переменной, передаваемой в качестве ссылочного параметра, или когда ее адрес передается в качестве параметра указателя.

## <a name="example"></a>Пример

Этот пример создает C4700, когда переменные t, u и v используются перед инициализацией, и показывает тип значения мусора, которое может быть получено. Переменные x, y и z не вызывают предупреждение, так как они инициализируются перед использованием:

```cpp
// c4700.cpp
// compile by using: cl /EHsc /W4 c4700.cpp
#include <iostream>

// function takes an int reference to initialize
void initialize(int& i)
{
    i = 21;
}

int main()
{
    int s, t, u, v;   // Danger, uninitialized variables

    s = t + u + v;    // C4700: t, u, v used before initialization
    std::cout << "Value in s: " << s << std::endl;

    int w, x;         // Danger, uninitialized variables
    initialize(x);    // fix: call function to init x before use
    int y{10};        // fix: initialize y, z when declared
    int z{11};        // This C++11 syntax is recommended over int z = 11;

    w = x + y + z;    // Okay, all values initialized before use
    std::cout << "Value in w: " << w << std::endl;
}
```

При выполнении этого кода t, u и v не инициализируются, а выходные данные для s являются непредсказуемыми:

```Output
Value in s: 37816963
Value in w: 42
```
