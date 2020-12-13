---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4391'
title: Предупреждение компилятора (уровень 1) C4391
ms.date: 11/04/2016
f1_keywords:
- C4391
helpviewer_keywords:
- C4391
ms.assetid: 95c6182c-fae9-4174-8f7b-98aa352e68ca
ms.openlocfilehash: 89c3babcf78dd47188cb03afa629a5aeda923fc7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97339918"
---
# <a name="compiler-warning-level-1-c4391"></a>Предупреждение компилятора (уровень 1) C4391

"сигнатура": неправильный возвращаемый тип для подставляемой функции; требуется "тип"

Объявление функции для встроенного компилятора имело неправильный тип возвращаемого значения. Полученный образ может работать неправильно.

Чтобы устранить это предупреждение, исправьте объявление или удалите объявление и просто #include соответствующий файл заголовка.

Следующий пример приводит к возникновению ошибки C4391:

```cpp
// C4391.cpp
// compile with: /W1
// processor: x86
// uncomment the following line and delete the line that
// generated the warning to resolve
// #include "xmmintrin.h"

#ifdef  __cplusplus
extern "C" {
#endif

extern void _mm_load_ss(float *p);   // C4391

#ifdef  __cplusplus
}
#endif

int main()
{
}
```
