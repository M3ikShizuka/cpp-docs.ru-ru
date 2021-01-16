---
description: 'Дополнительные сведения: ___lc_locale_name_func'
title: ___lc_locale_name_func
ms.date: 1/14/2021
api_name:
- ___lc_locale_name_func
- _o____lc_locale_name_func
api_location:
- msvcrt.dll
- msvcr110.dll
- msvcr100.dll
- msvcr90.dll
- msvcr120.dll
- msvcr80.dll
- msvcr110_clr0400.dll
- api-ms-win-crt-private-l1-1-0.dll
- api-ms-win-crt-locale-l1-1-0.dll
api_type:
- DLLExport
topic_type:
- apiref
f1_keywords:
- ___lc_locale_name_func
helpviewer_keywords:
- ___lc_locale_name_func
ms.assetid: ef858308-872e-43de-95e0-9b1b4084343e
ms.openlocfilehash: 4747b64c0fc61e0f5d77eacb92c04c9f6d2e2759
ms.sourcegitcommit: 1cd8f8a75fd036ffa57bc70f3ca869042d8019d4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "98242869"
---
# <a name="___lc_locale_name_func"></a>___lc_locale_name_func

Внутренняя функция CRT. Получает имя текущего языкового стандарта потока.

## <a name="syntax"></a>Синтаксис

```cpp
wchar_t** ___lc_locale_name_func(void);
```

## <a name="return-value"></a>Возвращаемое значение

Указатель на строку, которая содержит имя текущего языкового стандарта потока.

## <a name="remarks"></a>Комментарии

`___lc_locale_name_func` — это внутренняя функция CRT, которая используется другими функциями CRT для получения текущего языкового стандарта из локального хранилища потока для данных CRT. Эти сведения можно также получить с помощью функции [_get_current_locale](../c-runtime-library/reference/get-current-locale.md) или функций [setlocale, _wsetlocale](../c-runtime-library/reference/setlocale-wsetlocale.md).

Внутренние функции CRT связаны с конкретной реализацией и подлежат изменению в каждом выпуске. Мы не рекомендуем использовать их в коде.

По умолчанию глобальное состояние этой функции ограничивается приложением. Чтобы изменить это, см. раздел [глобальное состояние в CRT](global-state.md).

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|`___lc_locale_name_func`|crt\src\setlocal.h|

## <a name="see-also"></a>См. также

[_get_current_locale](../c-runtime-library/reference/get-current-locale.md)<br/>
[setlocale, _wsetlocale](../c-runtime-library/reference/setlocale-wsetlocale.md)<br/>
[_create_locale, _wcreate_locale](../c-runtime-library/reference/create-locale-wcreate-locale.md)<br/>
[_free_locale](../c-runtime-library/reference/free-locale.md)
