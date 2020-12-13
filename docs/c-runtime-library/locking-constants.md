---
description: 'Дополнительные сведения: _locking константы'
title: Константы _locking
ms.date: 11/04/2016
f1_keywords:
- _LK_RLCK
- _LK_NBLCK
- _LK_LOCK
- _LK_NBRLCK
- _LK_UNLCK
helpviewer_keywords:
- LK_UNLCK constant
- LK_NBRLCK constant
- _LK_NBRLCK constant
- _LK_NBLCK constant
- _LK_LOCK constant
- LK_NBLCK constant
- _LK_UNLCK constant
- LK_RLCK constant
- _LK_RLCK constant
- LK_LOCK constant
ms.assetid: c3dc92c8-60e3-4d29-9f50-5d217627c8ad
ms.openlocfilehash: 143c1416dada19e0bd35f1607d77826d98817879
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97331033"
---
# <a name="_locking-constants"></a>Константы _locking

## <a name="syntax"></a>Синтаксис

```
#include <sys/locking.h>
```

## <a name="remarks"></a>Remarks

Аргумент *mode* в вызове функции `_locking` определяет, какое действие блокировки будет выполняться.

Аргумент *mode* должен быть одной из следующих констант манифеста.

|Значение|Описание|
|-|-|
| `_LK_LOCK`  | Блокирует указанные байты. Если заблокировать байты не удается, функция попытается повторить блокировку снова через 1 секунду. Если после 10 попыток байты все равно не удается заблокировать, функция возвращает ошибку.  |
| `_LK_RLCK`  | Эквивалентно `_LK_LOCK`.  |
|`_LK_NBLCK`  | Блокирует указанные байты. Если байты не удается заблокировать, функция возвращает ошибку.  |
| `_LK_NBRLCK`  | Эквивалентно `_LK_NBLCK`.  |
| `_LK_UNLCK`  | Разблокирует указанные байты. (Байты должны быть ранее заблокированы.)  |

## <a name="see-also"></a>См. также раздел

[_locking](../c-runtime-library/reference/locking.md)<br/>
[Глобальные константы](../c-runtime-library/global-constants.md)
