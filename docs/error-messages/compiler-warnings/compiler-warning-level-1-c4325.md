---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4325'
title: Предупреждение компилятора (уровень 1) C4325
ms.date: 08/27/2018
f1_keywords:
- C4325
helpviewer_keywords:
- C4325
ms.assetid: 8127a08c-d626-481b-aa7b-04a3fdc9a9ec
ms.openlocfilehash: 17e14d4909e4b76d6a0a71d6e77fad1d01e3f41b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97311595"
---
# <a name="compiler-warning-level-1-c4325"></a>Предупреждение компилятора (уровень 1) C4325

> атрибуты для стандартного раздела "*раздел*" пропущены

## <a name="remarks"></a>Комментарии

Вы не можете изменить атрибуты стандартного раздела. Пример:

```cpp
#pragma section(".sdata", long)
```

Это приведет к перезаписи `.sdata` стандартного раздела, который использует **`short`** тип данных с **`long`** типом данных.

Стандартные разделы, атрибуты которых вы не можете изменить:

- . Data

- . sdata

- . BSS

- . SBSS

- .text

- . const

- . сконст

- . rdata

- . срдата

Дополнительные разделы можно добавить позже.

## <a name="see-also"></a>См. также раздел

[раздела](../../preprocessor/section.md)
