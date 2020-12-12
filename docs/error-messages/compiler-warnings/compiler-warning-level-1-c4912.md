---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4912'
title: Предупреждение компилятора (уровень 1) C4912
ms.date: 11/04/2016
f1_keywords:
- C4912
helpviewer_keywords:
- C4912
ms.assetid: ba1f1a66-8c20-4792-9ac8-43e49f729ae2
ms.openlocfilehash: 85300716894f9c69815bf40ebb7d93ee29d8684b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97291445"
---
# <a name="compiler-warning-level-1-c4912"></a>Предупреждение компилятора (уровень 1) C4912

"атрибут": поведение атрибута во вложенных UDT не определено

Атрибуты, применяемые ко вложенным UDT (определяемым пользователем типам, которые могут быть typedef, union или struct), могут игнорироваться.

В следующем коде показано, как это предупреждение может быть создано:

```cpp
// C4912.cpp
// compile with: /W1
#include <windows.h>
[emitidl, module(name="xx")];

[object, uuid("00000000-0000-0000-0000-000000000002")]
__interface IMy
{
};

[coclass, default(IMy), appobject, uuid("00000000-0000-0000-0000-000000000001")]
class CMy : public IMy
{
   [export, v1_enum] typedef enum myEnum { k3_1 = 1, k3_2 = 2 } myEnumv;   // C4912
};
int main()
{
}
```
