---
description: 'Дополнительные сведения о: pop_macro pragma'
title: Прагма pop_macro
ms.date: 08/29/2019
f1_keywords:
- vc-pragma.pop_macro
- pop_macro_CPP
helpviewer_keywords:
- pop_macro pragma
- pragmas, pop_macro
ms.assetid: 3b5489d0-69ba-4c66-b572-2748af0f12bb
ms.openlocfilehash: 395e107586b9534b2e9db616f30ddd88b15b93ec
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97325710"
---
# <a name="pop_macro-pragma"></a>Прагма pop_macro

Задает в качестве значения макроса *имени макроса* значение в верхней части стека для этого макроса.

## <a name="syntax"></a>Синтаксис

> **#pragma pop_macro (** "*Macro-Name*" **)**

## <a name="remarks"></a>Комментарии

Прежде чем выполнять **pop_macro**, необходимо выдать [push_macro](../preprocessor/push-macro.md) для *макроопределения-Name* .

## <a name="example"></a>Пример

```cpp
// pragma_directives_pop_macro.cpp
// compile with: /W1
#include <stdio.h>
#define X 1
#define Y 2

int main() {
   printf("%d",X);
   printf("\n%d",Y);
   #define Y 3   // C4005
   #pragma push_macro("Y")
   #pragma push_macro("X")
   printf("\n%d",X);
   #define X 2   // C4005
   printf("\n%d",X);
   #pragma pop_macro("X")
   printf("\n%d",X);
   #pragma pop_macro("Y")
   printf("\n%d",Y);
}
```

```Output
1
2
1
2
1
3
```

## <a name="see-also"></a>См. также раздел

[Директивы pragma и ключевое слово __pragma](../preprocessor/pragma-directives-and-the-pragma-keyword.md)
