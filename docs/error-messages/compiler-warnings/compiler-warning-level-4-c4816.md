---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 4) C4816'
title: Предупреждение компилятора (уровень 4) C4816
ms.date: 11/04/2016
f1_keywords:
- C4816
helpviewer_keywords:
- C4816
ms.assetid: 60f730ae-d942-4db9-ab97-41d4a874d8da
ms.openlocfilehash: b48f6f0141966a75a9a15f3f172a32fd81a52354
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97330492"
---
# <a name="compiler-warning-level-4-c4816"></a>Предупреждение компилятора (уровень 4) C4816

param: параметр имеет массив нулевого размера, который будет сокращен (если только объект не передается по ссылке)

Параметр объекта с нулевым размером массива не был передан по ссылке. Массив не будет скопирован при передаче объекта.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C4816.

```cpp
// C4816.cpp
// compile with: /W4
#include <stdio.h>

extern "C" int printf_s(const char *, ...);

#pragma warning(disable : 4200)

struct S1
{
    int i;
    char cArr[];
};

void TestErr(S1 s1)   // C4816 param with zero-array
                      // not passed by reference
{
    printf_s("%d %c %c\n", s1.i, s1.cArr[0], s1.cArr[1]);
}

void TestOk(S1 &s1)
{
    printf_s("%d %c %c\n", s1.i, s1.cArr[0], s1.cArr[1]);
}

int main()
{
    S1 myS_1 = { 6, 'a', 'b', 'c' };
    TestErr(myS_1);
    TestOk(myS_1);
}
```
