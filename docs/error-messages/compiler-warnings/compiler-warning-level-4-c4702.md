---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 4) C4702'
title: Предупреждение компилятора (уровень 4) C4702
ms.date: 11/04/2016
f1_keywords:
- C4702
helpviewer_keywords:
- C4702
ms.assetid: d8198c1e-8762-42a6-9e6b-cb568b7a1686
ms.openlocfilehash: 9a171641a2c923083471d510e27fbdb3ebd08832
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97133800"
---
# <a name="compiler-warning-level-4-c4702"></a>Предупреждение компилятора (уровень 4) C4702

недостижимый код

Это предупреждение является результатом действий по согласованности компилятора, выполненных для Visual Studio .NET 2003: недостижимый код. Когда компилятор (серверная система) обнаруживает недостижимый код, он создает C4702, предупреждение уровня 4.

Для кода, который является допустимым в версиях Visual Studio .NET 2003 и Visual Studio .NET Visual C++, удалите недостижимый код или убедитесь, что весь исходный код доступен для потока выполнения.

## <a name="examples"></a>Примеры

Следующий пример приводит к возникновению ошибки C4702.

```cpp
// C4702.cpp
// compile with: /W4
#include <stdio.h>

int main() {
   return 1;
   printf_s("I won't print.\n");   // C4702 unreachable
}
```

При компиляции с параметром **/GX**, **/EHC**, **/EHsc** или **/ехак** и использованием внешних функций c код может стать недостижимым, так как предполагается, что внешние функции c не вызывают исключение, поэтому блок catch недоступен.  Если вы считаете, что это предупреждение является недопустимым, так как функция может вызывать, компилировать с **/EHa** или **/EHs** в зависимости от вызываемого исключения.

Дополнительные сведения см. в разделе [/EH (модель обработки исключений)](../../build/reference/eh-exception-handling-model.md) .

Следующий пример приводит к возникновению ошибки C4702.

```cpp
// C4702b.cpp
// compile with: /W4 /EHsc
#include <iostream>

using namespace std;
extern "C" __declspec(dllexport) void Function2(){}

int main() {
   try {
      Function2();
   }
   catch (...) {
      cout << "Exp: Function2!" << endl;   // C4702
   }
}
```
