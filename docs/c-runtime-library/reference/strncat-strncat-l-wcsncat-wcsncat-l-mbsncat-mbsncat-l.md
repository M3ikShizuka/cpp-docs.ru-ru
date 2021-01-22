---
description: 'Дополнительные сведения: strncat, _strncat_l, wcsncat, _wcsncat_l, _mbsncat, _mbsncat_l'
title: strncat, _strncat_l, wcsncat, _wcsncat_l, _mbsncat, _mbsncat_l
ms.date: 1/20/2021
api_name:
- strncat
- _strncat_l
- _mbsncat
- _mbsncat_l
- wcsncat
- wcsncat_l
- _o__mbsncat
- _o__mbsncat_l
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
- api-ms-win-crt-string-l1-1-0.dll
- ntoskrnl.exe
- api-ms-win-crt-private-l1-1-0.dll
api_type:
- DLLExport
topic_type:
- apiref
f1_keywords:
- _tcsncat_l
- _wcsncat_l
- _tcsnccat_l
- _mbsncat
- _strncat_l
- strncat
- _tcsnccat
- _mbsncat_l
- _ftcsncat
- wcsncat
- _tcsncat
helpviewer_keywords:
- concatenating strings
- ftcsncat function
- tcsncat_l function
- _tcsnccat_l function
- _tcsncat function
- strncat function
- _ftcsncat function
- mbsncat function
- mbsncat_l function
- strings [C++], appending
- wcsncat function
- tcsnccat function
- tcsnccat_l function
- _tcsnccat function
- string concatenation [C++]
- appending strings
- characters [C++], appending to strings
- _mbsncat function
- _tcsncat_l function
- _mbsncat_l function
- tcsncat function
ms.openlocfilehash: 4b5ae812560cb42498ebed71bb9b8791581ef332
ms.sourcegitcommit: 3d9cfde85df33002e3b3d7f3509ff6a8dc4c0a21
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/21/2021
ms.locfileid: "98667023"
---
# <a name="strncat-_strncat_l-wcsncat-_wcsncat_l-_mbsncat-_mbsncat_l"></a>strncat, _strncat_l, wcsncat, _wcsncat_l, _mbsncat, _mbsncat_l

Добавляет символы строки. Доступны более безопасные версии этих функций, см. раздел `[strncat_s, _strncat_s_l, wcsncat_s, _wcsncat_s_l, _mbsncat_s, _mbsncat_s_l` ] (strncat-s-strncat-s-l-wcsncat-s-wcsncat-s-l-mbsncat-s-mbsncat-s-l.md).

> [!IMPORTANT]
> **`_mbsncat`** и **`_mbsncat_l`** не могут использоваться в приложениях, выполняемых в среда выполнения Windows. Дополнительные сведения: [Функции CRT, которые не поддерживаются в приложениях универсальной платформы Windows](../../cppcx/crt-functions-not-supported-in-universal-windows-platform-apps.md).

## <a name="syntax"></a>Синтаксис

```C
char *strncat(
   char *strDest,
   const char *strSource,
   size_t count
);
wchar_t *wcsncat(
   wchar_t *strDest,
   const wchar_t *strSource,
   size_t count
);
unsigned char *_mbsncat(
   unsigned char *strDest,
   const unsigned char *strSource,
   size_t count
);
unsigned char *_mbsncat_l(
   unsigned char *strDest,
   const unsigned char *strSource,
   size_t count,
   _locale_t locale
);
template <size_t size>
char *strncat(
   char (&strDest)[size],
   const char *strSource,
   size_t count
); // C++ only
template <size_t size>
wchar_t *wcsncat(
   wchar_t (&strDest)[size],
   const wchar_t *strSource,
   size_t count
); // C++ only
template <size_t size>
unsigned char *_mbsncat(
   unsigned char (&strDest)[size],
   const unsigned char *strSource,
   size_t count
); // C++ only
template <size_t size>
unsigned char *_mbsncat_l(
   unsigned char (&strDest)[size],
   const unsigned char *strSource,
   size_t count,
   _locale_t locale
); // C++ only
```

### <a name="parameters"></a>Параметры

*`strDest`*\
Строка назначения, завершающаяся нуль-символом.

*`strSource`*\
Исходная строка, завершающаяся символом NULL.

*`count`*\
Количество символов для добавления.

*`locale`*\
Используемый языковой стандарт.

## <a name="return-value"></a>Возвращаемое значение

Возвращает указатель на целевую строку символов. Нет зарезервированных возвращаемых значений для указания ошибки.

## <a name="remarks"></a>Примечания

**`strncat`** Функция добавляет не больше первых *`count`* символов *`strSource`* в *`strDest`* . Начальный символ *`strSource`* перезаписи завершающего нуль символа в *`strDest`* . Если символ NULL появляется в *`strSource`* перед *`count`* добавлением символов, **`strncat`** добавляет все символы из *`strSource`* , вплоть до символа null. Если *`count`* значение больше, чем длина *`strSource`* , используется вместо параметра length *`strSource`* *`count`* . Во всех случаях результирующая строка завершается нуль-символом. Если копирование производится между перекрывающимися строками, поведение не определено.

> [!IMPORTANT]
> **`strncat`** не проверяет наличие достаточного места в *`strDest`* , поэтому возможная причина переполнения буфера. Обратите внимание, что *`count`* ограничивает число добавленных символов; это не ограничение на размер *`strDest`* . См. пример ниже. Дополнительные сведения см. в разделе [Как избежать переполнения буфера](/windows/win32/SecBP/avoiding-buffer-overruns).

**`wcsncat`** и **`_mbsncat`** — это версии с расширенными символами и многобайтовой кодировкой **`strncat`** . Строковые аргументы и возвращаемое значение **`wcsncat`** являются строками расширенных символов; это строки **`_mbsncat`** многобайтовых символов. В остальном эти три функции ведут себя идентично.

На выходное значение влияет параметр **`LC_CTYPE`** категории языкового стандарта. Дополнительные сведения см. в разделе [`setlocale`](setlocale-wsetlocale.md) . Версии этих функций без **`_l`** суффикса используют текущий языковой стандарт для этого поведения, зависящего от языкового стандарта. Версии с **`_l`** суффиксом идентичны, за исключением того, что они используют переданный параметр языкового стандарта. Для получения дополнительной информации см. [Locale](../../c-runtime-library/locale.md).

В C++ эти функции имеют шаблонные перегрузки. Дополнительные сведения см. в разделе [Безопасные перегрузки шаблонов](../../c-runtime-library/secure-template-overloads.md).

По умолчанию глобальное состояние этой функции ограничивается приложением. Чтобы изменить это, см. раздел [глобальное состояние в CRT](../global-state.md).

### <a name="generic-text-routine-mappings"></a>Универсальное текстовое сопоставление функций

|`TCHAR.H `ассемблер|`_UNICODE & _MBCS` не определено|`_MBCS` определяется|`_UNICODE` определяется|
|---------------------|------------------------------------|--------------------|-----------------------|
|**`_tcsncat`**|**`strncat`**|**`_mbsnbcat`**|**`wcsncat`**|
|**`_tcsncat_l`**|**`_strncat_l`**|**`_mbsnbcat_l`**|**`_wcsncat_l`**|

> [!NOTE]
> **`_strncat_l`** и не **`_wcsncat_l`** имеют зависимости от языкового стандарта и не предназначены для непосредственного вызова. Они предоставляются для внутреннего использования **`_tcsncat_l`** .

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|**`strncat`**|\<string.h>|
|**`wcsncat`**|\<string.h> или \<wchar.h>|
|**`_mbsncat`**|\<mbstring.h>|
|**`_mbsncat_l`**|\<mbstring.h>|

Дополнительные сведения о совместимости см. в разделе [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="example"></a>Пример

```C
// crt_strncat.c
// Use strcat and strncat to append to a string.
#include <stdlib.h>

#define MAXSTRINGLEN 39

char string[MAXSTRINGLEN+1];
// or char *string = malloc(MAXSTRINGLEN+1);

void BadAppend( char suffix[], int n )
{
   strncat( string, suffix, n );
}

void GoodAppend( char suffix[], size_t n )
{
   strncat( string, suffix, __min( n, MAXSTRINGLEN-strlen(string)) );
}

int main( void )
{
   string[0] = '\0';
   printf( "string can hold up to %d characters\n", MAXSTRINGLEN );

   strcpy( string, "This is the initial string!" );
   // concatenate up to 20 characters...
   BadAppend( "Extra text to add to the string...", 20 );
   printf( "After BadAppend :  %s (%d chars)\n", string, strlen(string) );

   strcpy( string, "This is the initial string!" );
   // concatenate up to 20 characters...
   GoodAppend( "Extra text to add to the string...", 20 );
   printf( "After GoodAppend:  %s (%d chars)\n", string, strlen(string) );
}
```

### <a name="output"></a>Выходные данные

```Output
string can hold up to 39 characters
After BadAppend :  This is the initial string!Extra text to add to (47 chars)
After GoodAppend:  This is the initial string!Extra text t (39 chars)
```

Обратите внимание, что **бадаппенд** привел к переполнению буфера.

## <a name="see-also"></a>См. также раздел

[Управление строками](../../c-runtime-library/string-manipulation-crt.md)\
[`_mbsnbcat, _mbsnbcat_l`](mbsnbcat-mbsnbcat-l.md)\
[`strcat, wcscat, _mbscat`](strcat-wcscat-mbscat.md)\
[`strcmp, wcscmp, _mbscmp`](strcmp-wcscmp-mbscmp.md)\
[`strcpy, wcscpy, _mbscpy`](strcpy-wcscpy-mbscpy.md)\
[`strncmp, wcsncmp, _mbsncmp, _mbsncmp_l`](strncmp-wcsncmp-mbsncmp-mbsncmp-l.md)\
[`strncpy, _strncpy_l, wcsncpy, _wcsncpy_l, _mbsncpy, _mbsncpy_l`](strncpy-strncpy-l-wcsncpy-wcsncpy-l-mbsncpy-mbsncpy-l.md)\
[`_strnicmp, _wcsnicmp, _mbsnicmp, _strnicmp_l, _wcsnicmp_l, _mbsnicmp_l`](strnicmp-wcsnicmp-mbsnicmp-strnicmp-l-wcsnicmp-l-mbsnicmp-l.md)\
[`strrchr, wcsrchr, _mbsrchr, _mbsrchr_l`](strrchr-wcsrchr-mbsrchr-mbsrchr-l.md)\
[`_strset, _strset_l, _wcsset, _wcsset_l, _mbsset, _mbsset_l`](strset-strset-l-wcsset-wcsset-l-mbsset-mbsset-l.md)\
[`strspn, wcsspn, _mbsspn, _mbsspn_l`](strspn-wcsspn-mbsspn-mbsspn-l.md)\
[Языкового стандарта](../../c-runtime-library/locale.md)\
[Интерпретация последовательностей Multibyte-Character](../../c-runtime-library/interpretation-of-multibyte-character-sequences.md)\
