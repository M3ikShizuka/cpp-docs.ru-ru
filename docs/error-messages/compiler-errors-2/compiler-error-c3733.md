---
description: 'Дополнительные сведения о: Ошибка компилятора C3733'
title: Ошибка компилятора C3733
ms.date: 11/04/2016
f1_keywords:
- C3733
helpviewer_keywords:
- C3733
ms.assetid: 0cc1a9fe-1400-4be3-b35a-16435cba7a5a
ms.openlocfilehash: 768586c760a06c502a08a8a11b8a1ad4e33c4e93
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97245022"
---
# <a name="compiler-error-c3733"></a>Ошибка компилятора C3733

"событие": неправильный синтаксис для указания события COM; Вы забыли "__interface"?

Для события COM использован неправильный синтаксис. Чтобы устранить эту ошибку, измените тип события или исправьте синтаксис в соответствии с правилами событий COM.

Следующий пример приводит к возникновению ошибки C3733:

```
#define _ATL_ATTRIBUTES 1
#include "atlbase.h"
#include "atlcom.h"

[coclass, event_source(com), // change 'com' to 'native' to resolve
uuid("00000000-0000-0000-0000-000000000001")]
class A
{
   __event void func();   // C3733
};

int main()
{
}
```
