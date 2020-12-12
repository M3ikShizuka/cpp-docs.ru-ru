---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4747'
title: Предупреждение компилятора (уровень 1) C4747
ms.date: 11/04/2016
f1_keywords:
- C4747
helpviewer_keywords:
- C4747
ms.assetid: af37befd-ba1f-4bdc-96e1-a953f7a2ad9c
ms.openlocfilehash: e182f4fc6a270917bb0b7e348000a0f084183ba6
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97332201"
---
# <a name="compiler-warning-level-1-c4747"></a>Предупреждение компилятора (уровень 1) C4747

Вызов управляемой "EntryPoint": управляемый код не может выполняться при блокировке загрузчика, включая точку входа DLL и вызовы, достигнутые в точке входа DLL

Компилятор обнаружил (возможно) точку входа DLL, скомпилированную в MSIL.  Из-за потенциальных проблем при загрузке библиотеки DLL, точка входа которой была скомпилирована в MSIL, настоятельно не рекомендуется компилировать функцию точки входа DLL в MSIL.

Дополнительные сведения см. в разделе [Инициализация смешанных сборок](../../dotnet/initialization-of-mixed-assemblies.md) и [средств компоновщика ошибка LNK1306](../../error-messages/tool-errors/linker-tools-error-lnk1306.md).

### <a name="to-correct-this-error"></a>Исправление ошибки

1. Не компилируйте модуль с помощью **параметра/clr**.

1. Пометьте функцию точки входа значением `#pragma unmanaged` .

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C4747.

```cpp
// C4747.cpp
// compile with: /clr /c /W1
// C4747 expected
#include <windows.h>

// Uncomment the following line to resolve.
// #pragma unmanaged

BOOL WINAPI DllMain(HANDLE hInstance, ULONG Command, LPVOID Reserved) {
   return TRUE;
};
```
