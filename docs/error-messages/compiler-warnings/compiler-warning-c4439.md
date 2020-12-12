---
description: 'Дополнительные сведения о: предупреждение компилятора C4439'
title: Предупреждение компилятора C4439
ms.date: 11/04/2016
f1_keywords:
- C4439
helpviewer_keywords:
- C4439
ms.assetid: 9449958f-f407-4824-829b-9e092f2af97d
ms.openlocfilehash: 123f42ca495faeccc995dc1ac87572180d1dce70
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97180751"
---
# <a name="compiler-warning-c4439"></a>Предупреждение компилятора C4439

"функция": определение функции с управляемым типом в сигнатуре должно иметь __clrcallное соглашение о вызовах

Компилятор неявно заменяет соглашение о вызовах на [`__clrcall`](../../cpp/clrcall.md) . Чтобы устранить это предупреждение, удалите **`__cdecl`** **`__stdcall`** соглашение о вызовах или.

C4439 всегда выдается как ошибка. Это предупреждение можно отключить с помощью `#pragma warning` или **`/wd`** ; см. [предупреждение](../../preprocessor/warning.md) или [/w,/W0,/W1,/W2,/W3,/W4,/W1,/W2,/W3,/W4,/Wall,/WD,/We,/WO,/WV,/WX (уровень предупреждений)](../../build/reference/compiler-option-warning-level.md) для получения дополнительных сведений.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C4439.

```cpp
// C4439.cpp
// compile with: /clr
void __stdcall f( System::String^ arg ) {}   // C4439
void __clrcall f2( System::String^ arg ) {}   // OK
void f3( System::String^ arg ) {}   // OK
```
