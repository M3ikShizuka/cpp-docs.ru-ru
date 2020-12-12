---
description: 'Дополнительные сведения: _RTC_NumErrors'
title: _RTC_NumErrors
ms.date: 11/04/2016
api_name:
- _RTC_NumErrors
api_location:
- msvcrt.dll
- msvcr80.dll
- msvcr90.dll
- msvcr100.dll
- msvcr100_clr0400.dll
- msvcr110.dll
- msvcr110_clr0400.dll
- msvcr120.dll
- msvcr120_clr0400.dll
- ucrtbase.dll
api_type:
- DLLExport
topic_type:
- apiref
f1_keywords:
- _RTC_NumErrors
- RTC_NumErrors
helpviewer_keywords:
- run-time errors
- _RTC_NumErrors function
- RTC_NumErrors function
ms.assetid: 7e82adae-38e2-4f8b-bc0b-37bda8109fd1
ms.openlocfilehash: df103f5aada8c896669b82abc1b65621597acf1a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97168713"
---
# <a name="_rtc_numerrors"></a>_RTC_NumErrors

Возвращает общее количество ошибок, которое может быть обнаружено путем проверки на ошибки во время выполнения (RTC). Это число можно использовать в качестве элемента управления в **`for`** цикле, где каждое значение в цикле передается в [_RTC_GetErrDesc](rtc-geterrdesc.md).

## <a name="syntax"></a>Синтаксис

```C

int _RTC_NumErrors( void );
```

## <a name="return-value"></a>Возвращаемое значение

Целое число, представляющее общее количество ошибок, которое может быть обнаружено проверками на ошибки во время выполнения Visual C++.

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|**_RTC_NumErrors**|\<rtcapi.h>|

Дополнительные сведения см. в разделе [Совместимость](../../c-runtime-library/compatibility.md).

## <a name="libraries"></a>Библиотеки

Все версии [библиотек времени выполнения языка C](../../c-runtime-library/crt-library-features.md).

## <a name="see-also"></a>См. также раздел

[_RTC_GetErrDesc](rtc-geterrdesc.md)<br/>
[Проверка ошибок во время выполнения](../../c-runtime-library/run-time-error-checking.md)<br/>
