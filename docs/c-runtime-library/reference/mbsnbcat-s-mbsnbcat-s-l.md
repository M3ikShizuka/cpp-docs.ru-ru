---
title: '`_mbsnbcat_s`, `_mbsnbcat_s_l`'
description: Описание API для Microsoft Visual C++ `_mbsnbcat_s` и `_mbsnbcat_s_l` функций
ms.date: 12/2/2020
api_name:
- _mbsnbcat_s_l
- _mbsnbcat_s
- _o__mbsnbcat_s
- _o__mbsnbcat_s_l
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
- api-ms-win-crt-multibyte-l1-1-0.dll
- api-ms-win-crt-private-l1-1-0.dll
api_type:
- DLLExport
topic_type:
- apiref
f1_keywords:
- _mbsnbcat_s
- mbsnbcat_s
- _mbsnbcat_s_l
- mbsnbcat_s_l
helpviewer_keywords:
- _tcsncat function
- mbsnbcat_s function
- _mbsnbcat_s function
- _mbsnbcat_s_l function
- _tcsncat_s_l function
- tcsncat_s_l function
- mbsnbcat_s_l function
- tcsncat function
ms.assetid: 2c9e9be7-d979-4a54-8ada-23428b6648a9
ms.openlocfilehash: c7198d806d8ebe077b423ff2135b5bdcf66ffac6
ms.sourcegitcommit: 9c45483572db4470fe5db5a7b596d5770303098c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/02/2020
ms.locfileid: "96523118"
---
# <a name="_mbsnbcat_s-_mbsnbcat_s_l"></a>`_mbsnbcat_s`, `_mbsnbcat_s_l`

Добавляет в строку многобайтовых символов, в первую очередь, первые **n** байтов другой многобайтовой строки. Это версии [ `_mbsnbcat` , `_mbsnbcat_l` ](mbsnbcat-mbsnbcat-l.md) которые имеют улучшения безопасности, как описано в разделе [функции безопасности в CRT](../../c-runtime-library/security-features-in-the-crt.md).

> [!IMPORTANT]
> Этот API нельзя использовать в приложениях, выполняемых в среде выполнения Windows. Дополнительные сведения: [Функции CRT, которые не поддерживаются в приложениях универсальной платформы Windows](../../cppcx/crt-functions-not-supported-in-universal-windows-platform-apps.md).

## <a name="syntax"></a>Синтаксис

```C
errno_t _mbsnbcat_s(
   unsigned char *dest,
   size_t sizeInBytes,
   const unsigned char *src,
   size_t count
);
errno_t _mbsnbcat_s_l(
   unsigned char *dest,
   size_t sizeInBytes,
   const unsigned char *src,
   size_t count,
   _locale_t locale
);
template <size_t size>
errno_t _mbsnbcat_s(
   unsigned char (&dest)[size],
   const unsigned char *src,
   size_t count
); // C++ only
template <size_t size>
errno_t _mbsnbcat_s_l(
   unsigned char (&dest)[size],
   const unsigned char *src,
   size_t count,
   _locale_t locale
); // C++ only
```

### <a name="parameters"></a>Параметры

*`dest`*\
Многобайтовая строка назначения, завершаемая нуль-символом.

*`sizeInBytes`*\
Размер *`dest`* буфера в байтах.

*`src`*\
Исходная многобайтовая строка, завершаемая нуль-символом.

*`count`*\
Число байтов, из которых *`src`* необходимо добавить к *`dest`* .

*`locale`*\
Используемый языковой стандарт.

## <a name="return-value"></a>Возвращаемое значение

Ноль в случае успешного выполнения; в противном случае — код ошибки.

### <a name="error-conditions"></a>Ситуации, которые могут привести к ошибке

|**`dest`**|*`sizeInBytes`*|*`src`*|Возвращаемое значение|
|------------|-------------------|-----------|------------------|
|**`NULL`**|any|any|**`EINVAL`**|
|Любой|<= 0|any|**`EINVAL`**|
|Любой|any|**`NULL`**|**`EINVAL`**|

Если возникает какое-либо из условий ошибки, функция создает ошибку недопустимого параметра, как описано в разделе [Проверка параметров](../../c-runtime-library/parameter-validation.md). Если ошибка обработана, функция возвращает **`EINVAL`** и устанавливает значение **errno** переводится в **`EINVAL`** .

## <a name="remarks"></a>Примечания

**`_mbsnbcat_s`** Функция добавляет в (не *`dest`* более) первые *`count`* байты *`src`* . Если байт, непосредственно предшествующий символу NULL в, *`dest`* является старшим байтом, он перезаписывается начальным байтом *`src`* . В противном случае начальный байт объекта *`src`* перезаписывает завершающий нуль символ *`dest`* . Если в *`src`* предшествующих байтах отображается нуль-байт *`count`* , **`_mbsnbcat_s`** добавляет все байты из *`src`* , вплоть до символа null. Если *`count`* значение больше, чем длина *`src`* , используется вместо параметра length *`src`* *`count`* . Результирующая строка завершается нуль-символом. Если копирование производится между перекрывающимися строками, поведение не определено.

На выходное значение влияет параметр **`LC_CTYPE`** категории языкового стандарта; дополнительные сведения см. в разделе [setlocale, _wsetlocale](setlocale-wsetlocale.md) . Версии этих функций идентичны, за исключением того, что у тех, кто не имеет **`_l`** суффикса, используется текущий языковой стандарт, а **`_l`** вместо них используется переданный параметр языкового стандарта. Для получения дополнительной информации см. [Locale](../../c-runtime-library/locale.md).

В C++ использование этих функций упрощено с помощью перегрузок шаблонов. Перегрузки могут определять длину буфера автоматически, что устраняет необходимость указывать аргумент размера, и они могут автоматически использовать более новые, более безопасные функции для замены старых и менее безопасных функций. Дополнительные сведения см. в разделе [Безопасные перегрузки шаблонов](../../c-runtime-library/secure-template-overloads.md).

Версии отладочной библиотеки этих функций сначала заполняют буфер 0xFE. Чтобы отключить это поведение, используйте [`_CrtSetDebugFillThreshold`](crtsetdebugfillthreshold.md) .

По умолчанию глобальное состояние этой функции ограничивается приложением. Чтобы изменить это, см. раздел [глобальное состояние в CRT](../global-state.md).

### <a name="generic-text-routine-mappings"></a>Универсальное текстовое сопоставление функций

|`Tchar.h` ассемблер|`_UNICODE` и `_MBCS` не определено|`_MBCS` определяется|`_UNICODE` определяется|
|---------------------|--------------------------------------|--------------------|-----------------------|
|**`_tcsncat_s`**|[strncat_s](strncat-s-strncat-s-l-wcsncat-s-wcsncat-s-l-mbsncat-s-mbsncat-s-l.md)|**`_mbsnbcat_s`**|[wcsncat_s](strncat-s-strncat-s-l-wcsncat-s-wcsncat-s-l-mbsncat-s-mbsncat-s-l.md)|
|**`_tcsncat_s_l`**|**`_strncat_s_l`**|**`_mbsnbcat_s_l`**|**`_wcsncat_s_l`**|

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|**`_mbsnbcat_s`**|\<mbstring.h>|
|**`_mbsnbcat_s_l`**|\<mbstring.h>|

Дополнительные сведения о совместимости см. в разделе [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="see-also"></a>См. также

[Управление строками](../../c-runtime-library/string-manipulation-crt.md)\
[`_mbsnbcmp`, `_mbsnbcmp_l`](mbsnbcmp-mbsnbcmp-l.md)\
[`_strncnt`, `_wcsncnt`, `_mbsnbcnt`, `_mbsnbcnt_l`, `_mbsnccnt`, `_mbsnccnt_l`](strncnt-wcsncnt-mbsnbcnt-mbsnbcnt-l-mbsnccnt-mbsnccnt-l.md)\
[`_mbsnbcpy`, `_mbsnbcpy_l`](mbsnbcpy-mbsnbcpy-l.md)\
[`_mbsnbcpy_s`, `_mbsnbcpy_s_l`](mbsnbcpy-s-mbsnbcpy-s-l.md)\
[`_mbsnbset`, `_mbsnbset_l`](mbsnbset-mbsnbset-l.md)\
[`strncat`, `_strncat_l`, `wcsncat`, `_wcsncat_l`, `_mbsncat`, `_mbsncat_l`](strncat-strncat-l-wcsncat-wcsncat-l-mbsncat-mbsncat-l.md)\
[`strncat_s`, `_strncat_s_l`, `wcsncat_s`, `_wcsncat_s_l`, `_mbsncat_s`, `_mbsncat_s_l`](strncat-s-strncat-s-l-wcsncat-s-wcsncat-s-l-mbsncat-s-mbsncat-s-l.md)
