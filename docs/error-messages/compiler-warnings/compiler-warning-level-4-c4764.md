---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 4) C4764'
title: Предупреждение компилятора (уровень 4) C4764
ms.date: 11/04/2016
f1_keywords:
- C4764
helpviewer_keywords:
- C4764
ms.assetid: 7bd4296f-966b-484c-bf73-8dbc8e85b4a9
ms.openlocfilehash: d694987893d0e6fc6f04b13551a4c86141222192
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97330502"
---
# <a name="compiler-warning-level-4-c4764"></a>Предупреждение компилятора (уровень 4) C4764

Для перехваченных объектов выравнивание не может превышать 16 байт

Задано выравнивание, превышающее 16 байтов. На некоторых платформах при возникновении исключения функции принудительно устанавливается выравнивание стека, не превышающее 16 байтов.

## <a name="example"></a>Пример

При компиляции следующего примера выдается предупреждение C4764:

```cpp
// C4764.cpp
// compile with: /W4 /EHsc
// processor: x64 IPF
#include <stdio.h>

class A
{
public:
    int x;
};

typedef __declspec(align(32)) A ALIGNEDA;

int main()
{
    ALIGNEDA a;
    try
    {
        a.x = 15;
        throw a;
    }
    catch (ALIGNEDA b) // can’t align b to > 16 bytes
    {
        printf_s("%d\n", b.x);
    }
}   // C4764
```
