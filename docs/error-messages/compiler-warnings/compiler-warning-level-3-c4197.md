---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 3) C4197'
title: Предупреждение компилятора (уровень 3) C4197
ms.date: 11/04/2016
f1_keywords:
- C4197
helpviewer_keywords:
- C4197
ms.assetid: f766feef-82b0-4d81-8a65-33628c7db196
ms.openlocfilehash: f52c37e28ce681b96158b7e1f10fef3e9f121522
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97344215"
---
# <a name="compiler-warning-level-3-c4197"></a>Предупреждение компилятора (уровень 3) C4197

"тип": постоянное приведение volatile верхнего уровня игнорируется

Компилятор обнаружил приведение к типу r-value, дополненному типом " [volatile](../../cpp/volatile-cpp.md)" или приведением типа r-значения к какому-либо типу с квалификатором volatile. Согласно стандарту C (6.5.3), свойства, связанные с квалифицированными типами, имеют смысл только для выражений с l-значением.

Следующий пример приводит к возникновению ошибки C4197:

```cpp
// C4197.cpp
// compile with: /W3
#include <stdio.h>
#include <signal.h>
#include <stdlib.h>

void sigproc(int);
struct S
{
   int i;
} s;

int main()
{
   signal(SIGINT, sigproc);
   s.i = 1;
   S *pS = &s;
   for ( ; (volatile int)pS->i ; )   // C4197
      break;
   // for ( ; *(volatile int *)&pS->i ; )   // OK
   //    break;
}

void sigproc(int) // ctrl-C
{
   signal(SIGINT, sigproc);
   s.i = 0;
}
```
