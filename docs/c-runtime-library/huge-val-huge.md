---
description: 'Дополнительные сведения: HUGE_VAL, _HUGE'
title: HUGE_VAL, _HUGE
ms.date: 11/04/2016
api_name:
- _HUGE
api_location:
- msvcrt.dll
api_type:
- DLLExport
topic_type:
- apiref
f1_keywords:
- _HUGE
- HUGE_VAL
helpviewer_keywords:
- _HUGE constant
- HUGE_VAL constant
- double value
ms.assetid: 3f044b45-02cd-46b2-b1de-87fd0441dd6a
ms.openlocfilehash: c4109b61b9af65681ca2a006a3839e3d0338fa73
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97253147"
---
# <a name="huge_val-_huge"></a>HUGE_VAL, _HUGE

## <a name="syntax"></a>Синтаксис

```
#include <math.h>
```

## <a name="remarks"></a>Remarks

`HUGE_VAL` является максимальным представимым значением double. Это значение возвращается многими математическими функциями времени выполнения при возникновении ошибки. Для некоторых функций возвращается значение –`HUGE_VAL`. `HUGE_VAL` определяется как `_HUGE`, но математические функции времени выполнения возвращают `HUGE_VAL`. Для согласованности в коде также необходимо использовать значение `HUGE_VAL`.

## <a name="see-also"></a>См. также раздел

[Глобальные константы](../c-runtime-library/global-constants.md)
