---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4272'
title: Предупреждение компилятора (уровень 1) C4272
ms.date: 11/04/2016
f1_keywords:
- C4272
helpviewer_keywords:
- C4272
ms.assetid: 0d6c1de4-2eef-42c4-b861-c221f8b495ef
ms.openlocfilehash: a44e3a4121c1d01b15af47b0b4eefb1f982423bd
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97266121"
---
# <a name="compiler-warning-level-1-c4272"></a>Предупреждение компилятора (уровень 1) C4272

"функция": помечена как __declspec (dllimport); При импорте функции необходимо указать собственное соглашение о вызовах.

Экспорт функции, помеченной соглашением о вызовах [__clrcall](../../cpp/clrcall.md) , является ошибкой, и компилятор выдает это предупреждение при попытке импортировать функцию, помеченную как `__clrcall` .

Следующий пример приводит к возникновению ошибки C4272:

```cpp
// C4272.cpp
// compile with: /c /W1 /clr
__declspec(dllimport) void __clrcall Test();   // C4272
__declspec(dllimport) void Test2();   // OK
```
