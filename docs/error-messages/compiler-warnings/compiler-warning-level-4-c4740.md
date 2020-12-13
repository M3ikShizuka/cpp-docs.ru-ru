---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 4) C4740'
title: Предупреждение компилятора (уровень 4) C4740
ms.date: 11/04/2016
f1_keywords:
- C4740
helpviewer_keywords:
- C4740
ms.assetid: 85528969-966a-44b4-8a2f-971704c64477
ms.openlocfilehash: 31c25660177931e468681f3e563a9885ca1faa01
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97330533"
---
# <a name="compiler-warning-level-4-c4740"></a>Предупреждение компилятора (уровень 4) C4740

Постановка потока в встроенный код ASM или из него подавляет глобальную оптимизацию

При переходе в или из **`asm`** блока для этой функции отключается глобальная оптимизация.

Следующий пример приводит к возникновению ошибки C4740:

```cpp
// C4740.cpp
// compile with: /O2 /W4
// processor: x86
int main() {
   __asm jmp tester
   tester:;
}
```
