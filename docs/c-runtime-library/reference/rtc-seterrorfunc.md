---
description: 'Дополнительные сведения: _RTC_SetErrorFunc'
title: _RTC_SetErrorFunc
ms.date: 11/04/2016
api_name:
- _RTC_SetErrorFunc
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
- RTC_SetErrorFunc
- _RTC_SetErrorFunc
helpviewer_keywords:
- RTC_SetErrorFunc function
- _RTC_SetErrorFunc function
ms.assetid: b2292722-0d83-4092-83df-3d5b19880666
ms.openlocfilehash: 454fd54e0960e8ce52c94b4e4a1e0a93ea99d3eb
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97268942"
---
# <a name="_rtc_seterrorfunc"></a>_RTC_SetErrorFunc

Назначает функцию в качестве обработчика для сообщений о проверке на ошибки во время выполнения (RTC). Эта функция является устаревшей; Вместо этого используйте **_RTC_SetErrorFuncW** .

## <a name="syntax"></a>Синтаксис

```C
_RTC_error_fn _RTC_SetErrorFunc(
   _RTC_error_fn function
);
```

### <a name="parameters"></a>Параметры

*function*<br/>
Адрес функции, которая будет обрабатывать проверки на ошибки во время выполнения.

## <a name="return-value"></a>Возвращаемое значение

Ранее определенная функция обработки ошибок. Если ранее определенная функция отсутствует, возвращает **значение NULL**.

## <a name="remarks"></a>Комментарии

Не используйте эту функцию. Вместо этого используйте **_RTC_SetErrorFuncW**. Она сохраняется только для обратной совместимости.

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|**_RTC_SetErrorFunc**|\<rtcapi.h>|

Дополнительные сведения см. в разделе [Совместимость](../../c-runtime-library/compatibility.md).

## <a name="libraries"></a>Библиотеки

Все версии [библиотек времени выполнения языка C](../../c-runtime-library/crt-library-features.md).

## <a name="see-also"></a>См. также раздел

[_CrtDbgReport, _CrtDbgReportW](crtdbgreport-crtdbgreportw.md)<br/>
[Проверка ошибок во время выполнения](../../c-runtime-library/run-time-error-checking.md)<br/>
