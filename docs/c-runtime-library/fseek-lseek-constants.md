---
description: 'Дополнительные сведения: fseek, _lseek константы'
title: fseek, _lseek Constants
ms.date: 11/04/2016
f1_keywords:
- SEEK_END
- SEEK_SET
- SEEK_CUR
helpviewer_keywords:
- SEEK_SET constant
- SEEK_END constant
- SEEK_CUR constant
ms.assetid: 9deeb13e-5aa3-4c33-80d8-721c80a4de9d
ms.openlocfilehash: be12597682074f610b0a69395146b400fed4d6b2
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97319821"
---
# <a name="fseek-_lseek-constants"></a>fseek, _lseek Constants

## <a name="syntax"></a>Синтаксис

```
#include <stdio.h>
```

## <a name="remarks"></a>Remarks

Аргумент *origin* определяет исходную позицию и может быть одной из следующих констант манифеста.

|Константа|Значение|
|--------------|-------------|
|`SEEK_END`|Конец файла|
|`SEEK_CUR`|Текущая позиция файлового указателя|
|`SEEK_SET`|Начало файла|

## <a name="see-also"></a>См. также раздел

[fseek, _fseeki64](../c-runtime-library/reference/fseek-fseeki64.md)<br/>
[_lseek, _lseeki64](../c-runtime-library/reference/lseek-lseeki64.md)<br/>
[Глобальные константы](../c-runtime-library/global-constants.md)
