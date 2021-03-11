---
description: 'Дополнительные сведения о: fprintf, _fprintf_l, fwprintf, _fwprintf_l'
title: fprintf, _fprintf_l, fwprintf, _fwprintf_l
ms.date: 3/9/2021
api_name:
- fwprintf
- fprintf
- _fprintf_l
- _fwprintf_l
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
- fprintf
- fwprintf
- _ftprintf
helpviewer_keywords:
- _fwprintf_l function
- fprintf function
- fprintf_l function
- _fprintf_l function
- _ftprintf function
- fwprintf function
- ftprintf_l function
- ftprintf function
- _ftprintf_l function
- print formatted data to streams
- fwprintf_l function
ms.openlocfilehash: 4e56182a9e32beb826cb7257cc2199e3ebe19e77
ms.sourcegitcommit: b04b39940b0c1e265f80fc1951278fdb05a1b30a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/10/2021
ms.locfileid: "102621962"
---
# <a name="fprintf-_fprintf_l-fwprintf-_fwprintf_l"></a>fprintf, _fprintf_l, fwprintf, _fwprintf_l

Печатает форматированные данные в поток. Существуют более безопасные версии этих функций. См. раздел [fprintf_s, _fprintf_s_l, fwprintf_s, _fwprintf_s_l](fprintf-s-fprintf-s-l-fwprintf-s-fwprintf-s-l.md).

## <a name="syntax"></a>Синтаксис

```C
int fprintf(
   FILE *stream,
   const char *format [,
   argument ]...
);
int _fprintf_l(
   FILE *stream,
   const char *format,
   locale_t locale [,
   argument ]...
);
int fwprintf(
   FILE *stream,
   const wchar_t *format [,
   argument ]...
);
int _fwprintf_l(
   FILE *stream,
   const wchar_t *format,
   locale_t locale [,
   argument ]...
);
```

### <a name="parameters"></a>Параметры

*вышестоящий*<br/>
Указатель на структуру **FILE**.

*format*<br/>
Строка управления форматом.

*argument*<br/>
Необязательные аргументы.

*locale*<br/>
Используемый языковой стандарт.

## <a name="return-value"></a>Возвращаемое значение

**fprintf** возвращает число записанных байтов. **fwprintf** возвращает число записанных расширенных символов. В случае ошибки вывода каждая из этих функций возвращает отрицательное значение. Если *Stream* или *Format* имеет **значение NULL**, эти функции вызывают обработчик недопустимых параметров, как описано в разделе [Проверка параметров](../../c-runtime-library/parameter-validation.md). Если выполнение может быть продолжено, функции возвращают значение-1 и **задают значение** **еинвал**. Строка формата не проверяется на допустимость символов форматирования, как при использовании **fprintf_s** или **fwprintf_s**.

Дополнительные сведения об этих и других кодах ошибок см. в разделе [_doserrno, errno, _sys_errlist и _sys_nerr](../../c-runtime-library/errno-doserrno-sys-errlist-and-sys-nerr.md).

## <a name="remarks"></a>Remarks

**fprintf** форматирует и выводит последовательность символов и значений в *поток* вывода. Каждый *аргумент* функции (если таковой имеется) преобразуется и выводится в соответствии с соответствующей спецификацией формата в *формате*. Для **fprintf** аргумент *Format* имеет тот же синтаксис и использует его в **printf**.

**fwprintf** — это версия **fprintf** для расширенных символов; в **fwprintf** *Format* является строкой расширенных символов. Эти функции ведут себя одинаково, если поток открыт в режиме ANSI. **fprintf** в настоящее время не поддерживает вывод в поток Юникода.

Версии этих функций с суффиксом **_l** идентичны за исключением того, что они используют переданный параметр языкового стандарта вместо локали текущего потока.

> [!IMPORTANT]
> Убедитесь, что *format* не является строкой, определяемой пользователем.
>
>
> Начиная с Windows 10 версии 2004 (сборка 19041), `printf` семейство функций выводит в соответствии с правилами IEEE 754 только округленные числа с плавающей запятой. В предыдущих версиях Windows полностью непредставленные числа с плавающей запятой, которые заканчиваются на "5", всегда округляются. IEEE 754 указывает, что они должны округляться до ближайшей четной цифры (также называемой "округление банка"). Например, оба значения `printf("%1.0f", 1.5)` и `printf("%1.0f", 2.5)` должны округляться в 2. Ранее 1,5 бы округлялись до 2 и 2,5, округляя до 3. Это изменение влияет только на точное представление чисел. Например, 2,35 (который, когда представлен в памяти, находится ближе к 2.35000000000000008), по-своему округляется до 2,4. Округление, выполненное этими функциями, теперь также учитывает режим округления с плавающей запятой, установленный [`fesetround`](fegetround-fesetround2.md) . Ранее округление всегда выбрало `FE_TONEAREST` поведение. Это изменение влияет только на программы, созданные с помощью Visual Studio 2019 версии 16,2 и более поздних версий. Чтобы использовать устаревшее поведение округления с плавающей точкой, свяжите с ["legacy_stdio_float_rounding. obj"](../link-options.md).

### <a name="generic-text-routine-mappings"></a>Универсальное текстовое сопоставление функций

|Подпрограмма TCHAR.H|_UNICODE и _MBCS не определены|_MBCS определено|_UNICODE определено|
|---------------------|------------------------------------|--------------------|-----------------------|
|**_ftprintf**|**fprintf**|**fprintf**|**fwprintf**|
|**_ftprintf_l**|**_fprintf_l**|**_fprintf_l**|**_fwprintf_l**|

Дополнительные сведения см. в разделе [Спецификации формата](../../c-runtime-library/format-specification-syntax-printf-and-wprintf-functions.md).

## <a name="requirements"></a>Требования

|Функция|Обязательный заголовок|
|--------------|---------------------|
|**fprintf**, **_fprintf_l**|\<stdio.h>|
|**fwprintf**, **_fwprintf_l**|\<stdio.h> или \<wchar.h>|

Дополнительные сведения о совместимости см. в статье [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="example"></a>Пример

```C
// crt_fprintf.c
/* This program uses fprintf to format various
* data and print it to the file named FPRINTF.OUT. It
* then displays FPRINTF.OUT on the screen using the system
* function to invoke the operating-system TYPE command.
*/

#include <stdio.h>
#include <process.h>

FILE *stream;

int main( void )
{
   int    i = 10;
   double fp = 1.5;
   char   s[] = "this is a string";
   char   c = '\n';

   fopen_s( &stream, "fprintf.out", "w" );
   fprintf( stream, "%s%c", s, c );
   fprintf( stream, "%d\n", i );
   fprintf( stream, "%f\n", fp );
   fclose( stream );
   system( "type fprintf.out" );
}
```

```Output
this is a string
10
1.500000
```

## <a name="see-also"></a>См. также раздел

[Потоковый ввод-вывод](../../c-runtime-library/stream-i-o.md)<br/>
[_cprintf, _cprintf_l, _cwprintf, _cwprintf_l](cprintf-cprintf-l-cwprintf-cwprintf-l.md)<br/>
[fscanf, _fscanf_l, fwscanf, _fwscanf_l](fscanf-fscanf-l-fwscanf-fwscanf-l.md)<br/>
[sprintf, _sprintf_l, swprintf, _swprintf_l, \_ _swprintf_l](sprintf-sprintf-l-swprintf-swprintf-l-swprintf-l.md)<br/>
[Синтаксис спецификации формата: функции printf и wprintf](../../c-runtime-library/format-specification-syntax-printf-and-wprintf-functions.md)<br/>
