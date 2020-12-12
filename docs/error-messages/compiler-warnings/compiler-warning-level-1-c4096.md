---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4096'
title: Предупреждение компилятора (уровень 1) C4096
ms.date: 11/04/2016
f1_keywords:
- C4096
helpviewer_keywords:
- C4096
ms.assetid: abf3cca2-2f21-45d8-b025-6b513b00681e
ms.openlocfilehash: 2d787a2de5974b16fb962c17530532480d993fd6
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97278042"
---
# <a name="compiler-warning-level-1-c4096"></a>Предупреждение компилятора (уровень 1) C4096

"a": интерфейс не является COM-интерфейсом; не будет выдаваться в IDL

Определение интерфейса, которое может быть предназначено в качестве COM-интерфейса, не было определено как COM-интерфейс, и поэтому не будет выдаваться в файл IDL.

Атрибуты списка, указывающие, что интерфейс является COM-интерфейсом, см. в разделе [атрибуты интерфейса](../../windows/attributes/interface-attributes.md) .

Следующий пример приводит к возникновению ошибки C4096:

```cpp
// C4096.cpp
// compile with: /W1 /LD
#include "windows.h"
[module(name="xx")];

// [object, uuid("00000000-0000-0000-0000-000000000001")]
__interface a
{
};

[coclass, uuid("00000000-0000-0000-0000-000000000002")]
struct b : a
{
};   // C4096, remove coclass or uncomment object
```
