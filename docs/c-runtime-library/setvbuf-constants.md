---
description: 'Дополнительные сведения: константы setvbuf'
title: Константы setvbuf
ms.date: 11/04/2016
f1_keywords:
- _IOFBF
- _IONBF
- _IOLBF
helpviewer_keywords:
- _IOFBF constant
- IOFBF constant
- IONBF constant
- _IOLBF constant
- IOLBF constant
- _IONBF constant
ms.assetid: a6ec4dd5-1f24-498c-871a-e874cd28d33c
ms.openlocfilehash: 375c692f4437bd60c84e37c857e078d9386ffb1c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97277015"
---
# <a name="setvbuf-constants"></a>Константы setvbuf

## <a name="syntax"></a>Синтаксис

```
#include <stdio.h>
```

## <a name="remarks"></a>Remarks

Эти константы представляют тип буфера для `setvbuf`.

Возможные значения определяются следующими константами манифеста:

|Константа|Значение|
|--------------|-------------|
|`_IOFBF`|Полная буферизация. Используется буфер, указанный в вызове функции `setvbuf`, и его размер равен указанному в вызове функции `setvbuf`. Если указатель буфера имеет значение **NULL**, используется автоматически выделенный буфер указанного размера.|
|`_IOLBF`|Эквивалентно `_IOFBF`.|
|`_IONBF`|Буфер не используется, независимо от аргументов в вызове функции `setvbuf`.|

## <a name="see-also"></a>См. также раздел

[setbuf](../c-runtime-library/reference/setbuf.md)<br/>
[Глобальные константы](../c-runtime-library/global-constants.md)
