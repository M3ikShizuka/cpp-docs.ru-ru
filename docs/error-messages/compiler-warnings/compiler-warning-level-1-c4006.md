---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4006'
title: Предупреждение компилятора (уровень 1) C4006
ms.date: 11/04/2016
f1_keywords:
- C4006
helpviewer_keywords:
- C4006
ms.assetid: f1a59819-0fd2-4361-8e3a-99e4b514b8e1
ms.openlocfilehash: 1d0b38e2ac3d224f26a0a52ac2d7f2343a1f955d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97335977"
---
# <a name="compiler-warning-level-1-c4006"></a>Предупреждение компилятора (уровень 1) C4006

\#для undef требуется идентификатор

Директива `#undef` не указывает идентификатор для отмены. Директива игнорируется. Чтобы устранить это предупреждение, не забудьте указать идентификатор. Следующий пример приводит к возникновению ошибки C4006.

```cpp
// C4006.cpp
// compile with: /W1
#undef   // C4006

// try..
// #undef TEST

int main() {
}
```
