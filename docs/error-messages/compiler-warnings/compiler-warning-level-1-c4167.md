---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4167'
title: Предупреждение компилятора (уровень 1) C4167
ms.date: 11/04/2016
f1_keywords:
- C4167
helpviewer_keywords:
- C4167
ms.assetid: 74a420bd-9371-4167-b1ee-74dd8680f97b
ms.openlocfilehash: 8d0b08ea4d97c6e85f5e07ce4844abdae7afafbd
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97266992"
---
# <a name="compiler-warning-level-1-c4167"></a>Предупреждение компилятора (уровень 1) C4167

"функция": недоступна в качестве подставляемой функции

Директива **#pragma function** пытается принудить компилятор выполнить стандартный вызов функции, для которой необходимо использовать встроенную форму. Директива pragma игнорируется.

Чтобы устранить это предупреждение, удалите директиву **#pragma function**.

## <a name="example"></a>Пример

```cpp
// C4167.cpp
// compile with: /W1
#include <malloc.h>
#pragma function(_alloca )   // C4167: _alloca() is intrinsic only
int main(){}
```
