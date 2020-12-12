---
description: 'Дополнительные сведения: ToLower, _tolower, товловер, _tolower_l, _towlower_l'
title: tolower, _tolower, towlower, _tolower_l, _towlower_l
ms.date: 4/2/2020
api_name:
- _tolower_l
- towlower
- tolower
- _tolower
- _towlower_l
- _o__tolower
- _o__tolower_l
- _o__towlower_l
- _o_tolower
- _o_towlower
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
- ntdll.dll
- ucrtbase.dll
- api-ms-win-crt-string-l1-1-0.dll
- ntoskrnl.exe
- api-ms-win-crt-private-l1-1-0.dll
api_type:
- DLLExport
topic_type:
- apiref
f1_keywords:
- _totlower
- tolower
- _tolower
- towlower
helpviewer_keywords:
- tolower_l function
- _tolower_l function
- totlower function
- string conversion, to different characters
- lowercase, converting to
- tolower function
- string conversion, case
- towlower function
- _tolower function
- _totlower function
- towlower_l function
- case, converting
- characters, converting
- _towlower_l function
ms.assetid: 86e0fc02-94ae-4472-9631-bf8e96f67b92
ms.openlocfilehash: 5b686d9b511fe4864724f85be78ac511a6351ef7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97318329"
---
# <a name="tolower-_tolower-towlower-_tolower_l-_towlower_l"></a>tolower, _tolower, towlower, _tolower_l, _towlower_l

Преобразует символ в строчный.

## <a name="syntax"></a>Синтаксис

```C
int tolower(
   int c
);
int _tolower(
   int c
);
int towlower(
   wint_t c
);
int _tolower_l(
   int c,
   _locale_t locale
);
int _towlower_l(
   wint_t c,
   _locale_t locale
);
```

### <a name="parameters"></a>Параметры

*c*<br/>
Символ для преобразования.

*locale*<br/>
Языковой стандарт для перевода в определенном языковом стандарте.

## <a name="return-value"></a>Возвращаемое значение

Каждая из этих подпрограмм преобразует копию *c* в нижний регистр, если преобразование возможно, и возвращает результат. Возвращаемое значение для указания ошибки не зарезервировано.

## <a name="remarks"></a>Комментарии

Каждая из этих подпрограмм преобразует указанную прописную букву в строчную, если это возможно и уместно. Преобразование регистра **товловер** зависит от языкового стандарта. Изменяются только символы, соответствующие текущему языковому стандарту. Функции без суффикса **_l** используют текущую национальную настройку. Версии этих функций с суффиксом **_l** принимают языковой стандарт в качестве параметра и используют его вместо текущего языкового стандарта. Для получения дополнительной информации см. [Locale](../../c-runtime-library/locale.md).

Чтобы **_tolower** придать ожидаемые результаты, [__isascii](isascii-isascii-iswascii.md) и [Upper](isupper-isupper-l-iswupper-iswupper-l.md) должны возвращать ненулевое значение.

По умолчанию глобальное состояние этой функции ограничивается приложением. Чтобы изменить это, см. раздел [глобальное состояние в CRT](../global-state.md).

### <a name="generic-text-routine-mappings"></a>Универсальное текстовое сопоставление функций

|Подпрограмма TCHAR.H|_UNICODE и _MBCS не определены|_MBCS определено|_UNICODE определено|
|---------------------|------------------------------------|--------------------|-----------------------|
|**_totlower**|**ToLower**|**_mbctolower**|**towlower**|
|**_totlower_l**|**_tolower_l**|**_mbctolower_l**|**_towlower_l**|

> [!NOTE]
> **_tolower_l** и **_towlower_l** не имеют зависимости от языкового стандарта и не предназначены для непосредственного вызова. Они предоставляются для внутреннего использования **_totlower_l**.

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|**ToLower**|\<ctype.h>|
|**_tolower**|\<ctype.h>|
|**towlower**|\<ctype.h> или \<wchar.h>|

Дополнительные сведения о совместимости см. в статье [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="example"></a>Пример

См. пример в разделе [Функции to](../../c-runtime-library/to-functions.md).

## <a name="see-also"></a>См. также раздел

[Преобразование данных](../../c-runtime-library/data-conversion.md)<br/>
[является, подпрограммы isw](../../c-runtime-library/is-isw-routines.md)<br/>
[в функции](../../c-runtime-library/to-functions.md)<br/>
[Локаль](../../c-runtime-library/locale.md)<br/>
[Интерпретация последовательностей Multibyte-Character](../../c-runtime-library/interpretation-of-multibyte-character-sequences.md)<br/>
