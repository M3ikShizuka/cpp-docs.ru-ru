---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4377'
title: Предупреждение компилятора (уровень 1) C4377
ms.date: 11/04/2016
f1_keywords:
- C4377
helpviewer_keywords:
- C4377
ms.assetid: a1c797b8-cd5e-4a56-b430-d07932e811cf
ms.openlocfilehash: 674bfb69a20c901f20509a7359ed408b0e38f479
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97185704"
---
# <a name="compiler-warning-level-1-c4377"></a>Предупреждение компилятора (уровень 1) C4377

собственные типы являются частными по умолчанию; -D1privatenativetypes запрещен является устаревшим

В предыдущих выпусках собственные типы в сборках были общедоступными по умолчанию, и был использован внутренний, недокументированный параметр компилятора (**/d1PrivateNativeTypes**), чтобы сделать их частными.

Все типы, native и CLR теперь являются частными по умолчанию в сборке, поэтому **/d1PrivateNativeTypes** больше не требуется.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C4377.

```cpp
// C4377.cpp
// compile with: /clr /d1PrivateNativeTypes /W1
// C4377 warning expected
int main() {}
```
