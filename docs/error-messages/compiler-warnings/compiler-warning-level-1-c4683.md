---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4683'
title: Предупреждение компилятора (уровень 1) C4683
ms.date: 08/27/2018
f1_keywords:
- C4683
helpviewer_keywords:
- C4683
ms.assetid: e6e77364-dba1-46dd-ae1d-03da23070bce
ms.openlocfilehash: e7f2c76e7f15bb7342e60b2aa390cf0bd1a8ce05
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97285244"
---
# <a name="compiler-warning-level-1-c4683"></a>Предупреждение компилятора (уровень 1) C4683

> "*функция*": источник события имеет параметр "out"; Будьте внимательны при подключении нескольких обработчиков событий

## <a name="remarks"></a>Комментарии

Если несколько приемников событий ожидают передачи данных в источник событий COM, значение параметра out можно игнорировать.

Имейте в виду, что утечка памяти произойдет в следующих ситуациях:

1. , Если метод имеет параметр out, выделенный внутренним образом, например BSTR *.

2. Значение, если событие содержит более одного обработчика (является многоадресным событием).

Причина утечки заключается в том, что параметр out будет задан более чем одним обработчиком, но возвращен в узел вызова только последним обработчиком.

## <a name="example"></a>Пример

В следующем примере создается C4683 и демонстрируется его устранение.

```cpp
// C4683.cpp
// compile with: /W1 /LD
#define _ATL_ATTRIBUTES 1
#include "atlbase.h"
#include "atlcom.h"

[ module(name="xx") ];

[ object ]
__interface I {
   HRESULT f([out] int* pi);
   // try the following line instead
   // HRESULT f(int* pi);
};

[ coclass, event_source(com) ]
struct E {
   __event __interface I;   // C4683
};
```
