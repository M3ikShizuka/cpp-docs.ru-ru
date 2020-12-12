---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4224'
title: Предупреждение компилятора (уровень 1) C4223
ms.date: 11/04/2016
f1_keywords:
- C4224
helpviewer_keywords:
- C4224
ms.assetid: 1531cae0-5040-49fd-b149-005bb5085391
ms.openlocfilehash: f9632ec80ee845da6933be22a6e446ac5251257f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97266407"
---
# <a name="compiler-warning-level-1-c4224"></a>Предупреждение компилятора (уровень 1) C4223

использовано нестандартное расширение: формальный параметр "идентификатор" ранее был определен как тип

Идентификатор ранее использовался как **`typedef`** . Это приводит к появлению предупреждения о совместимости ANSI ([/Za](../../build/reference/za-ze-disable-language-extensions.md)).

## <a name="example"></a>Пример

```cpp
// C4224.cpp
// compile with: /Za /W1 /LD
typedef int I;
void func ( int I );  // C4224
```
