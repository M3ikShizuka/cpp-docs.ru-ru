---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4794'
title: Предупреждение компилятора (уровень 1) C4794
ms.date: 11/04/2016
f1_keywords:
- C4794
helpviewer_keywords:
- C4794
ms.assetid: badc9c36-fa1a-4fec-929b-7bfda7a7b79f
ms.openlocfilehash: bd43a9fb1f7f2433a4e1d337d49c1921211a9e5d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97334957"
---
# <a name="compiler-warning-level-1-c4794"></a>Предупреждение компилятора (уровень 1) C4794

сегмент переменной из локальной памяти потока "переменная" изменен с "имя_раздела" на ".tls$"

Вы использовали [#pragma data_seg](../../preprocessor/data-seg.md) , чтобы поместить переменную tls в раздел, не начинающийся с ".tls$".

Раздел .tls$*x* раздел будет существовать в объектном файле, где определены переменные [__declspec(thread)](../../cpp/thread.md) . Раздел .tls в файле EXE или DLL будет получен из этих разделов.

## <a name="example"></a>Пример

В следующем примере возникает ошибка C4794.

```cpp
// C4794.cpp
// compile with: /W1 /c
#pragma data_seg(".someseg")
__declspec(thread) int i;   // C4794

// OK
#pragma data_seg(".tls$9")
__declspec(thread) int j;
```
