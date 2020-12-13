---
description: 'Дополнительные сведения: _get_wpgmptr'
title: _get_wpgmptr
ms.date: 4/2/2020
api_name:
- _get_wpgmptr
- _o__get_wpgmptr
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
- get_wpgmptr
- _get_wpgmptr
helpviewer_keywords:
- _wpgmptr global variable
- get_wpgmptr function
- wpgmptr global variable
- _get_wpgmptr function
ms.assetid: a77cdd13-2303-4b7c-9a60-8debdbef2011
ms.openlocfilehash: fdc2f17a2c4d43a762f9fbab6629e2524742f0ef
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97338926"
---
# <a name="_get_wpgmptr"></a>_get_wpgmptr

Возвращает текущее значение **_wpgmptr** глобальной переменной.

## <a name="syntax"></a>Синтаксис

```C
errno_t _get_wpgmptr(
   wchar_t **pValue
);
```

### <a name="parameters"></a>Параметры

*pValue*<br/>
Указатель на строку, заполняемую текущим значением переменной **_wpgmptr** .

## <a name="return-value"></a>Возвращаемое значение

Возвращает нуль в случае успеха или код ошибки в случае ошибки. Если параметр *pValue* имеет **значение NULL**, вызывается обработчик недопустимых параметров, как описано в разделе [Проверка параметров](../../c-runtime-library/parameter-validation.md). Если выполнение может быть продолжено, эта функция **устанавливает** **Еинвал** и возвращает **еинвал**.

## <a name="remarks"></a>Комментарии

Вызывайте **_get_wpgmptr** только в том случае, если программа имеет широкую точку входа, например **wmain ()** или **wWinMain ()**. **_Wpgmptr** глобальная переменная содержит полный путь к исполняемому файлу, связанному с процессом, в виде строки расширенных символов. Дополнительные сведения см. в разделе [_pgmptr _wpgmptr](../../c-runtime-library/pgmptr-wpgmptr.md).

По умолчанию глобальное состояние этой функции ограничивается приложением. Чтобы изменить это, см. раздел [глобальное состояние в CRT](../global-state.md).

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|**_get_wpgmptr**|\<stdlib.h>|

Дополнительные сведения о совместимости см. в разделе [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="see-also"></a>См. также раздел

[_get_pgmptr](get-pgmptr.md)<br/>
