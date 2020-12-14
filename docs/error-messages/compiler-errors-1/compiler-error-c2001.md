---
description: 'Дополнительные сведения о: Ошибка компилятора C2001'
title: Ошибка компилятора C2001
ms.date: 11/04/2016
f1_keywords:
- C2001
helpviewer_keywords:
- C2001
ms.assetid: 0c3a7821-d8e5-4398-ab5a-4116d46e8dda
ms.openlocfilehash: 81c033288ae673e95bc3454e2754d371f84225e5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97298634"
---
# <a name="compiler-error-c2001"></a>Ошибка компилятора C2001

Новая строка в константе

Строковая константа не может продолжаться на второй строке, если не выполнить следующие действия.

- Завершите первую строку с помощью обратной косой черты.

- Закройте строку в первой строке с двойной кавычкой и откройте строку в следующей строке с помощью еще одной двойной кавычки.

Завершение первой строки с \n не является достаточным.

## <a name="examples"></a>Примеры

Следующий пример приводит к возникновению ошибки C2001:

```cpp
// C2001.cpp
// C2001 expected
#include <stdio.h>

int main()
{
    printf_s("Hello,
             world");
    printf_s("Hello,\n
             world");
}
```

Пробелы в начале следующей строки после символа продолжения строки включаются в строковую константу. Ни один из приведенных выше примеров не внедряет символ новой строки в строковую константу. Можно встроить символ новой строки, как показано ниже:

```cpp
// C2001b.cpp
#include <stdio.h>

int main()
{
    printf_s("Hello,\n\
             world");

    printf_s("Hello,\
             \nworld");

    printf_s("Hello,\n"
             "world");

    printf_s("Hello,"
             "\nworld");

    printf_s("Hello,"
             " world");

    printf_s("Hello,\
             world");
}
```
