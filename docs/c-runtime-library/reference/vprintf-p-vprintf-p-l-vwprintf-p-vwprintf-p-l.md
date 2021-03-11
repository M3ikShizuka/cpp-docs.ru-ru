---
description: 'Дополнительные сведения: _vprintf_p, _vprintf_p_l, _vwprintf_p, _vwprintf_p_l'
title: _vprintf_p, _vprintf_p_l, _vwprintf_p, _vwprintf_p_l
ms.date: 3/9/2021
api_name:
- _vwprintf_p
- _vprintf_p
- _vprintf_p_l
- _vwprintf_p_l
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
- _vwprintf_p_l
- vprintf_p
- _vprintf_p_l
- _vwprintf_p
- vprintf_p_l
- vwprintf_p_l
- vwprintf_p
- vtprintf_p
- _vtprintf_p
- _vprintf_p
helpviewer_keywords:
- _vtprintf_p_l function
- _vtprintf_p function
- vtprintf_p function
- _vwprintf_p function
- _vwprintf_p_l function
- _vprintf_p function
- _vprintf_p_l function
- vprintf_p_l function
- vwprintf_p function
- vprintf_p function
- vtprintf_p_l function
- vwprintf_p_l function
- formatted text [C++]
ms.openlocfilehash: 7cefabeafc8ccdaac48b401dba12a6f688824ae6
ms.sourcegitcommit: b04b39940b0c1e265f80fc1951278fdb05a1b30a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/10/2021
ms.locfileid: "102621715"
---
# <a name="_vprintf_p-_vprintf_p_l-_vwprintf_p-_vwprintf_p_l"></a>_vprintf_p, _vprintf_p_l, _vwprintf_p, _vwprintf_p_l

Записывают форматированные выходные данные, используя указатель на список аргументов, и включает спецификацию порядка, в котором эти аргументы используются.

## <a name="syntax"></a>Синтаксис

```C
int _vprintf_p(
   const char *format,
   va_list argptr
);
int _vprintf_p_l(
   const char *format,
   locale_t locale,
   va_list argptr
);
int _vwprintf_p(
   const wchar_t *format,
   va_list argptr
);
int _vwprintf_p_l(
   const wchar_t *format,
   locale_t locale,
   va_list argptr
);
```

### <a name="parameters"></a>Параметры

*format*<br/>
Спецификация формата.

*аргптр*<br/>
Указатель на список аргументов.

*locale*<br/>
Используемый языковой стандарт.

Дополнительные сведения см. в разделе [Спецификации формата](../../c-runtime-library/format-specification-syntax-printf-and-wprintf-functions.md).

## <a name="return-value"></a>Возвращаемое значение

**_vprintf_p** и **_vwprintf_p** возвращают число записанных символов, не включая завершающий нуль-символ, или отрицательное значение, если возникает ошибка вывода.

## <a name="remarks"></a>Remarks

Каждая из этих функций принимает указатель на список аргументов, затем форматирует и записывает указанные данные в **stdout**. Эти функции отличаются от **vprintf_s** и **vwprintf_s** только тем, что они поддерживают возможность указания порядка, в котором используются аргументы. Дополнительные сведения см. в разделе [Позиционные параметры printf_p](../../c-runtime-library/printf-p-positional-parameters.md).

**_vwprintf_p** — это версия **_vprintf_p** для расширенных символов; Эти две функции ведут себя одинаково, если поток открыт в режиме ANSI. **_vprintf_p** в настоящее время не поддерживает вывод в поток Юникода.

Версии этих функций с суффиксом **_l** идентичны за исключением того, что они используют переданный параметр языкового стандарта вместо локали текущего потока.

> [!IMPORTANT]
> Убедитесь, что *format* не является строкой, определяемой пользователем. Дополнительные сведения см. в разделе [Как избежать переполнения буфера](/windows/win32/SecBP/avoiding-buffer-overruns).
> Начиная с Windows 10 версии 2004 (сборка 19041), `printf` семейство функций выводит в соответствии с правилами IEEE 754 только округленные числа с плавающей запятой. В предыдущих версиях Windows полностью непредставленные числа с плавающей запятой, которые заканчиваются на "5", всегда округляются. IEEE 754 указывает, что они должны округляться до ближайшей четной цифры (также называемой "округление банка"). Например, оба значения `printf("%1.0f", 1.5)` и `printf("%1.0f", 2.5)` должны округляться в 2. Ранее 1,5 бы округлялись до 2 и 2,5, округляя до 3. Это изменение влияет только на точное представление чисел. Например, 2,35 (который, когда представлен в памяти, находится ближе к 2.35000000000000008), по-своему округляется до 2,4. Округление, выполненное этими функциями, теперь также учитывает режим округления с плавающей запятой, установленный [`fesetround`](fegetround-fesetround2.md) . Ранее округление всегда выбрало `FE_TONEAREST` поведение. Это изменение влияет только на программы, созданные с помощью Visual Studio 2019 версии 16,2 и более поздних версий. Чтобы использовать устаревшее поведение округления с плавающей точкой, свяжите с ["legacy_stdio_float_rounding. obj"](../link-options.md).

Если параметр *Format* является пустым указателем или строка формата содержит недопустимые символы форматирования, вызывается обработчик недопустимых параметров, как описано в разделе [Проверка параметров](../../c-runtime-library/parameter-validation.md). Если выполнение может быть продолжено, функции возвращают значение-1 и **задают значение** **еинвал**.

### <a name="generic-text-routine-mappings"></a>Универсальное текстовое сопоставление функций

|Подпрограмма TCHAR.H|_UNICODE и _MBCS не определены|_MBCS определено|_UNICODE определено|
|---------------------|------------------------------------|--------------------|-----------------------|
|**_vtprintf_p**|**_vprintf_p**|**_vprintf_p**|**_vwprintf_p**|
|**_vtprintf_p_l**|**_vprintf_p_l**|**_vprintf_p_l**|**_vwprintf_p_l**|

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|Необязательные заголовки|
|-------------|---------------------|----------------------|
|**_vprintf_p**, **_vprintf_p_l**|\<stdio.h> и \<stdarg.h>|\<varargs.h>*|
|**_vwprintf_p**, **_vwprintf_p_l**|\<stdio.h> или \<wchar.h> , и \<stdarg.h>|\<varargs.h>*|

\* Требуется для совместимости с UNIX V.

Консоль не поддерживается в приложениях универсальная платформа Windows (UWP). Стандартные дескрипторы потока, связанные с консолью, **stdin**, **stdout** и **stderr**, должны быть перенаправляться до того, как функции времени выполнения C смогут использовать их в приложениях UWP. Дополнительные сведения о совместимости см. в статье [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="see-also"></a>См. также раздел

[Потоковый ввод-вывод](../../c-runtime-library/stream-i-o.md)<br/>
[Функции vprintf](../../c-runtime-library/vprintf-functions.md)<br/>
[_fprintf_p, _fprintf_p_l, _fwprintf_p, _fwprintf_p_l](fprintf-p-fprintf-p-l-fwprintf-p-fwprintf-p-l.md)<br/>
[_printf_p, _printf_p_l, _wprintf_p, _wprintf_p_l](printf-p-printf-p-l-wprintf-p-wprintf-p-l.md)<br/>
[_sprintf_p, _sprintf_p_l, _swprintf_p, _swprintf_p_l](sprintf-p-sprintf-p-l-swprintf-p-swprintf-p-l.md)<br/>
[vsprintf_s, _vsprintf_s_l, vswprintf_s, _vswprintf_s_l](vsprintf-s-vsprintf-s-l-vswprintf-s-vswprintf-s-l.md)<br/>
[va_arg, va_copy, va_end, va_start](va-arg-va-copy-va-end-va-start.md)<br/>
[_vfprintf_p, _vfprintf_p_l, _vfwprintf_p, _vfwprintf_p_l](vfprintf-p-vfprintf-p-l-vfwprintf-p-vfwprintf-p-l.md)<br/>
[_printf_p, _printf_p_l, _wprintf_p, _wprintf_p_l](printf-p-printf-p-l-wprintf-p-wprintf-p-l.md)<br/>
[printf_p позиционированные параметры](../../c-runtime-library/printf-p-positional-parameters.md)<br/>
