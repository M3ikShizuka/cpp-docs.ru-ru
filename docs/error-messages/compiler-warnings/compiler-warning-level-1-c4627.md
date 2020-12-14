---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4627'
title: Предупреждение компилятора (уровень 1) C4627
ms.date: 09/09/2018
f1_keywords:
- C4627
helpviewer_keywords:
- C4627
ms.assetid: 8840f3e6-b496-423a-8635-eb55d5f854a2
ms.openlocfilehash: fc4c6c3931775b090dfd4c7c2fd5fd97441d40d3
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97281448"
---
# <a name="compiler-warning-level-1-c4627"></a>Предупреждение компилятора (уровень 1) C4627

> "*HEADER_FILE*": пропущено при поиске использования предкомпилированного заголовка

Если в текущем исходном файле установлен параметр [/Yu \( use предкомпилированный заголовочный файл)](../../build/reference/yu-use-precompiled-header-file.md) , Компилятор пропускает все файлы в файле перед включением предкомпилированного заголовка. Предупреждение **C4627** создается в Visual Studio 2015 и более ранних версиях, если *HEADER_FILE* входит перед предкомпилированным файлом заголовка, а также если предкомпилированный заголовок не включает *HEADER_FILE*.

## <a name="example"></a>Пример

В этом примере показано, как может произойти ошибка, и показано, как ее исправить:

```cpp
// c4627.cpp
#include <iostream>       // C4627 - iostream not included by pch.h
#include "pch.h"          // precompiled header file that does not include iostream
// #include <iostream>    // To fix, move the iostream header include here from above
int main()
{
    std::cout << "std::cout is defined!\n";
}
```

## <a name="see-also"></a>См. также раздел

[Создание файлов предкомпилированных заголовков](../../build/creating-precompiled-header-files.md)
