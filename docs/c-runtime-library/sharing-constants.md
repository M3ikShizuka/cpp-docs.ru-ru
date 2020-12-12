---
description: 'Подробнее: Общие сведения о константах'
title: Совместное использование констант
ms.date: 11/04/2016
f1_keywords:
- _SH_DENYNO
- _SH_DENYRD
- _SH_DENYRW
- _SH_DENYWR
- _SH_COMPAT
helpviewer_keywords:
- _SH_DENYRW constant
- SH_DENYRD constant
- _SH_COMPAT constant
- _SH_DENYRD constant
- SH_DENYRW constant
- sharing constants
- SH_DENYNO constant
- _SH_DENYWR constant
- SH_DENYWR constant
- _SH_DENYNO constant
- SH_COMPAT constant
ms.assetid: 95fadc3a-55dc-473d-98b5-e8211900465d
ms.openlocfilehash: 7cda55d16a9b59c30e9fdbce47c565552839e792
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97176175"
---
# <a name="sharing-constants"></a>Совместное использование констант

Константы для режимов общего доступа к файлам.

## <a name="syntax"></a>Синтаксис

```
#include <share.h>
```

## <a name="remarks"></a>Remarks

Аргумент *shflag* определяет режим общего доступа и состоит из одной или нескольких констант манифеста. Их можно использовать в сочетании с аргументами *oflag* (см. [Константы файлов](../c-runtime-library/file-constants.md)).

В следующей таблице перечислены константы и их смысловые значения:

|Константа|Значение|
|--------------|-------------|
|`_SH_DENYRW`|Запрещает доступ к файлу для чтения и записи|
|`_SH_DENYWR`|Запрещает доступ к файлу для записи|
|`_SH_DENYRD`|Запрещает доступ к файлу для чтения|
|`_SH_DENYNO`|Разрешает доступ для чтения и записи|
|`_SH_SECURE`|Устанавливает безопасный режим (совместный доступ для чтения, монопольный доступ для записи)|

## <a name="see-also"></a>См. также раздел

[_sopen, _wsopen](../c-runtime-library/reference/sopen-wsopen.md)<br/>
[_fsopen, _wfsopen](../c-runtime-library/reference/fsopen-wfsopen.md)<br/>
[Глобальные константы](../c-runtime-library/global-constants.md)
