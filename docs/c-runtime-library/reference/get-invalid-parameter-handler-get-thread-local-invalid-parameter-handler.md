---
description: 'Дополнительные сведения: _get_invalid_parameter_handler, _get_thread_local_invalid_parameter_handler'
title: _get_invalid_parameter_handler, _get_thread_local_invalid_parameter_handler
ms.date: 4/2/2020
api_name:
- _get_invalid_parameter_handler
- _get_thread_local_invalid_parameter_handler
- _o__get_invalid_parameter_handler
- _o__get_thread_local_invalid_parameter_handler
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
- api-ms-win-crt-runtime-l1-1-0.dll
- api-ms-win-crt-private-l1-1-0.dll
api_type:
- DLLExport
topic_type:
- apiref
f1_keywords:
- _get_invalid_parameter_handler
- stdlib/_get_invalid_parameter_handler
- _get_thread_local_invalid_parameter_handler
- stdlib/_get_thread_local_invalid_parameter_handler
helpviewer_keywords:
- _get_thread_local_invalid_parameter_handler function
- _get_invalid_parameter_handler function
ms.assetid: a176da0e-38ca-4d99-92bb-b0e2b8072f53
ms.openlocfilehash: ecb39588ea2776d661f391596d3f482628eddd7a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97213381"
---
# <a name="_get_invalid_parameter_handler-_get_thread_local_invalid_parameter_handler"></a>_get_invalid_parameter_handler, _get_thread_local_invalid_parameter_handler

Получает функцию, которая вызывается, когда CRT обнаруживает недопустимый аргумент.

## <a name="syntax"></a>Синтаксис

```C
_invalid_parameter_handler _get_invalid_parameter_handler(void);
_invalid_parameter_handler _get_thread_local_invalid_parameter_handler(void);
```

## <a name="return-value"></a>Возвращаемое значение

Указатель на установленную в данный момент функцию обработчика недопустимого параметра или указатель NULL, если такая функция не задана.

## <a name="remarks"></a>Комментарии

Функция **_get_invalid_parameter_handler** получает текущий установленный в данный момент глобальный обработчик недопустимых параметров. Если глобальный обработчик недопустимого параметра не задан, возвращается указатель NULL. Аналогичным образом **_get_thread_local_invalid_parameter_handler** получает текущий локальный обработчик недопустимых параметров потока, для которого он вызывается, или указатель null, если обработчик не был задан. Дополнительные сведения об установке глобального и локального для потока обработчика недопустимого параметра см. в разделе [_set_invalid_parameter_handler, _set_thread_local_invalid_parameter_handler](set-invalid-parameter-handler-set-thread-local-invalid-parameter-handler.md).

Возвращаемый указатель на функцию обработчика недопустимого параметра имеет следующий тип:

```C
typedef void (__cdecl* _invalid_parameter_handler)(
    wchar_t const*,
    wchar_t const*,
    wchar_t const*,
    unsigned int,
    uintptr_t
    );
```

Дополнительные сведения об обработчике недопустимого параметра см. в описании прототипа в разделе [_set_invalid_parameter_handler, _set_thread_local_invalid_parameter_handler](set-invalid-parameter-handler-set-thread-local-invalid-parameter-handler.md).

По умолчанию глобальное состояние этой функции ограничивается приложением. Чтобы изменить это, см. раздел [глобальное состояние в CRT](../global-state.md).

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|**_get_invalid_parameter_handler**, **_get_thread_local_invalid_parameter_handler**|Ц \<stdlib.h><br /><br /> C++: \<cstdlib> или \<stdlib.h>|

Функции **_get_invalid_parameter_handler** и **_get_thread_local_invalid_parameter_handler** являются специфичными для Microsoft. Сведения о совместимости см. в разделе [Совместимость](../../c-runtime-library/compatibility.md).

## <a name="see-also"></a>См. также раздел

[_set_invalid_parameter_handler, _set_thread_local_invalid_parameter_handler](set-invalid-parameter-handler-set-thread-local-invalid-parameter-handler.md)<br/>
[Версии функций CRT с повышенной безопасностью](../../c-runtime-library/security-enhanced-versions-of-crt-functions.md)<br/>
