---
description: 'Дополнительные сведения: _get_dstbias'
title: _get_dstbias
ms.date: 4/2/2020
api_name:
- _get_dstbias
- __dstbias
- _o___dstbias
- _o__get_dstbias
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
- __dstbias
- _get_dstbias
- get_dstbias
helpviewer_keywords:
- __dstbias
- daylight saving time offset
- get_dstbias function
- _get_dstbias function
ms.assetid: e751358c-1ecc-411b-ae2c-81b2ec54ea45
ms.openlocfilehash: 00c5cef0e7c1e5e79cbcc2ce37a13e3f56d27029
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97341455"
---
# <a name="_get_dstbias"></a>_get_dstbias

Получает смещение перехода на зимнее время в секундах.

## <a name="syntax"></a>Синтаксис

```C
error_t _get_dstbias( int* seconds );
```

### <a name="parameters"></a>Параметры

*секунд*<br/>
Смещение перехода на зимнее время в секундах.

## <a name="return-value"></a>Возвращаемое значение

Нуль в случае успеха или **значение** пересчета при возникновении ошибки.

## <a name="remarks"></a>Комментарии

Функция **_get_dstbias** извлекает количество секунд в формате летнего времени в виде целого числа. Если действует переход на зимнее время, смещение по умолчанию составляет 3600 секунд. Это число соответствует одному часу (хотя в некоторых регионах может применяться смещение на два часа).

Если значение *секунд* равно **null**, вызывается обработчик недопустимых параметров, как описано в разделе [Проверка параметров](../../c-runtime-library/parameter-validation.md). Если выполнение может быть продолжено, эта функция **устанавливает** **Еинвал** и возвращает **еинвал**.

Рекомендуется использовать эту функцию вместо макроса **_dstbias** или устаревшей функции **__dstbias**.

По умолчанию глобальное состояние этой функции ограничивается приложением. Чтобы изменить это, см. раздел [глобальное состояние в CRT](../global-state.md).

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|**_get_dstbias**|\<time.h>|

Дополнительные сведения см. в разделе [Совместимость](../../c-runtime-library/compatibility.md).

## <a name="see-also"></a>См. также раздел

[Операции управления временем](../../c-runtime-library/time-management.md)<br/>
[errno, _doserrno, _sys_errlist, and _sys_nerr](../../c-runtime-library/errno-doserrno-sys-errlist-and-sys-nerr.md)<br/>
[_get_daylight](get-daylight.md)<br/>
[_get_timezone](get-timezone.md)<br/>
[_get_tzname](get-tzname.md)<br/>
