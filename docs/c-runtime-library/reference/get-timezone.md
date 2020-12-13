---
description: 'Дополнительные сведения: _get_timezone'
title: _get_timezone
ms.date: 4/2/2020
api_name:
- _get_timezone
- _o__get_timezone
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
- api-ms-win-crt-time-l1-1-0.dll
- api-ms-win-crt-private-l1-1-0.dll
api_type:
- DLLExport
topic_type:
- apiref
f1_keywords:
- _get_timezone
- get_timezone
helpviewer_keywords:
- time zones
- get_timezone function
- _get_timezone function
ms.assetid: 30ab0838-0ae9-4a2f-bfe6-a49ee443b21e
ms.openlocfilehash: 9fb42603d0b7d63cbbb18c4904c221cd2edeb0e0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97338967"
---
# <a name="_get_timezone"></a>_get_timezone

Извлекает разницу в секундах между временем в формате UTC и местным временем.

## <a name="syntax"></a>Синтаксис

```C
error_t _get_timezone(
    long* seconds
);
```

### <a name="parameters"></a>Параметры

*секунд*<br/>
Разница в секундах между временем в формате UTC и местным временем.

## <a name="return-value"></a>Возвращаемое значение

Нуль в случае успеха или **значение** пересчета при возникновении ошибки.

## <a name="remarks"></a>Комментарии

Функция **_get_timezone** извлекает разность в секундах между временем UTC и местным временем в виде целого числа. Значение по умолчанию — 28800 секунд (тихоокеанское время, на 8 часов отстающее от UTC).

Если значение *секунд* равно **null**, вызывается обработчик недопустимых параметров, как описано в разделе [Проверка параметров](../../c-runtime-library/parameter-validation.md). Если выполнение может быть продолжено, эта функция **устанавливает** **Еинвал** и возвращает **еинвал**.

По умолчанию глобальное состояние этой функции ограничивается приложением. Чтобы изменить это, см. раздел [глобальное состояние в CRT](../global-state.md).

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|**_get_timezone**|\<time.h>|

Дополнительные сведения см. в разделе [Совместимость](../../c-runtime-library/compatibility.md).

## <a name="see-also"></a>См. также раздел

[Операции управления временем](../../c-runtime-library/time-management.md)<br/>
[errno, _doserrno, _sys_errlist, and _sys_nerr](../../c-runtime-library/errno-doserrno-sys-errlist-and-sys-nerr.md)<br/>
[_get_daylight](get-daylight.md)<br/>
[_get_dstbias](get-dstbias.md)<br/>
[_get_tzname](get-tzname.md)<br/>
