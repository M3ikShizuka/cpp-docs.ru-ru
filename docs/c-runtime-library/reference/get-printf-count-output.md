---
description: 'Дополнительные сведения: _get_printf_count_output'
title: _get_printf_count_output
ms.date: 11/04/2016
api_name:
- _get_printf_count_output
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
- api-ms-win-crt-stdio-l1-1-0.dll
api_type:
- DLLExport
topic_type:
- apiref
f1_keywords:
- get_printf_count_output
- _get_printf_count_output
helpviewer_keywords:
- '%n format'
- get_printf_count_output function
- _get_printf_count_output function
ms.assetid: 850f9f33-8319-433e-98d8-6a694200d994
ms.openlocfilehash: fe5ee728b7bc8400cd93ec4e93131496d59334c5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97339008"
---
# <a name="_get_printf_count_output"></a>_get_printf_count_output

Указывает, поддерживают ли функции [printf, _printf_l, wprintf, _wprintf_l](printf-printf-l-wprintf-wprintf-l.md)-Family формат **% n** .

## <a name="syntax"></a>Синтаксис

```C
int _get_printf_count_output();
```

## <a name="return-value"></a>Возвращаемое значение

Не равно нулю, если **% n** поддерживается, 0, если **% n** не поддерживается.

## <a name="remarks"></a>Комментарии

Если **% n** не поддерживается (по умолчанию), при обнаружении **% n** в строке формата любой из функций **printf** вызовет обработчик недопустимого параметра, как описано в разделе [Проверка параметров](../../c-runtime-library/parameter-validation.md). Если поддержка **% n** включена (см. [_set_printf_count_output](set-printf-count-output.md)), то **% n** будет работать, как описано в разделе [синтаксис спецификации формата: функции printf и wprintf](../../c-runtime-library/format-specification-syntax-printf-and-wprintf-functions.md).

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|**_get_printf_count_output**|\<stdio.h>|

Дополнительные сведения о совместимости см. в статье [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="example"></a>Пример

См. пример для [_set_printf_count_output](set-printf-count-output.md).

## <a name="see-also"></a>См. также раздел

[_set_printf_count_output](set-printf-count-output.md)<br/>
