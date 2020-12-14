---
description: 'Дополнительные сведения: _CRT_DISABLE_PERFCRIT_LOCKS'
title: _CRT_DISABLE_PERFCRIT_LOCKS
ms.date: 11/04/2016
f1_keywords:
- _CRT_DISABLE_PERFCRIT_LOCKS
- CRT_DISABLE_PERFCRIT_LOCKS
helpviewer_keywords:
- CRT_DISABLE_PERFCRIT_LOCKS constant
- _CRT_DISABLE_PERFCRIT_LOCKS constant
ms.assetid: 36cc2d86-cdb1-4b2b-a03c-c0d3818e7c6f
ms.openlocfilehash: b96e29fad635ac9e7f3d622ace3c43bb26c8805a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97195688"
---
# <a name="_crt_disable_perfcrit_locks"></a>_CRT_DISABLE_PERFCRIT_LOCKS

Отключает критическую с точки зрения производительности блокировку в операциях ввода-вывода.

## <a name="syntax"></a>Синтаксис

```
#define _CRT_DISABLE_PERFCRIT_LOCKS
```

## <a name="remarks"></a>Remarks

Определение этого символа может улучшить производительность в однопоточных привязанных к вводу-выводу программах путем принудительного использования однопоточной модели ввода-вывода во всех операциях ввода-вывода. Подробнее см. [Производительность многопоточных библиотек](../c-runtime-library/multithreaded-libraries-performance.md).

## <a name="see-also"></a>См. также раздел

[Глобальные константы](../c-runtime-library/global-constants.md)
