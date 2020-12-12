---
description: 'Дополнительные сведения: _RTC_GetErrDesc'
title: _RTC_GetErrDesc
ms.date: 11/04/2016
api_name:
- _RTC_GetErrDesc
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
- RTC_GetErrDesc
- _RTC_GetErrDesc
helpviewer_keywords:
- run-time errors
- _RTC_GetErrDesc function
- RTC_GetErrDesc function
ms.assetid: 7994ec2b-5488-4fd4-806d-a166c9a9f927
ms.openlocfilehash: 5e9beccec5e13d6c2c00e3edaefec695a8e16737
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97168726"
---
# <a name="_rtc_geterrdesc"></a>_RTC_GetErrDesc

Возвращает краткое описание типа проверки на ошибки во время выполнения (RTC).

## <a name="syntax"></a>Синтаксис

```C
const char * _RTC_GetErrDesc(
   _RTC_ErrorNumber errnum
);
```

### <a name="parameters"></a>Параметры

*errnum*<br/>
Число от нуля до единицы и меньше значения, возвращаемого **_RTC_NumErrors**.

## <a name="return-value"></a>Возвращаемое значение

Строка символов, которая содержит краткое описание одного из типов ошибок, обнаруженного системой проверки на ошибки во время выполнения. Если ошибка меньше нуля или больше или равна значению, возвращенному [_RTC_NumErrors](rtc-numerrors.md), **_RTC_GetErrDesc** возвращает **значение NULL**.

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|**_RTC_GetErrDesc**|\<rtcapi.h>|

Дополнительные сведения см. в разделе [Совместимость](../../c-runtime-library/compatibility.md).

## <a name="libraries"></a>Библиотеки

Все версии [библиотек времени выполнения языка C](../../c-runtime-library/crt-library-features.md).

## <a name="see-also"></a>См. также раздел

[_RTC_NumErrors](rtc-numerrors.md)<br/>
[Проверка ошибок во время выполнения](../../c-runtime-library/run-time-error-checking.md)<br/>
