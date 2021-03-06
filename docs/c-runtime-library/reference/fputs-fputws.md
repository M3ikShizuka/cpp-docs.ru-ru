---
description: 'Дополнительные сведения о: fputs, fputws'
title: fputs, fputws
ms.date: 03/02/2021
api_name:
- fputs
- fputws
- _o_fputs
- _o_fputws
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
- api-ms-win-crt-private-l1-1-0.dll
api_type:
- DLLExport
topic_type:
- apiref
f1_keywords:
- fputs
- fputws
- _fputts
helpviewer_keywords:
- streams, writing strings to
- fputws function
- _fputts function
- fputs function
- fputts function
ms.openlocfilehash: 3b38f3c369a567c00f17a0f4d905de324100a3d4
ms.sourcegitcommit: c0c9cdae79f19655e809a4979227c51bb19cff63
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "102236794"
---
# <a name="fputs-fputws"></a>`fputs`, `fputws`

Записывает строку в поток.

## <a name="syntax"></a>Синтаксис

```C
int fputs(
   const char *str,
   FILE *stream
);
int fputws(
   const wchar_t *str,
   FILE *stream
);
```

### <a name="parameters"></a>Параметры

*`str`*\
Выходная строка.

*`stream`*\
Указатель на **`FILE`** структуру.

## <a name="return-value"></a>Возвращаемое значение

Каждая из этих функций возвращает неотрицательное значение при успешном выполнении. При возникновении ошибки **`fputs`** и **`fputws`** возвращает **`EOF`** . Если *`str`* или *`stream`* является пустым указателем, эти функции вызывают обработчик недопустимых параметров, как описано в разделе [Проверка параметров](../../c-runtime-library/parameter-validation.md). Если выполнение может быть продолжено, эти функции устанавливают **`errno`** в значение **`EINVAL`** , а затем возвращают **`EOF`** .

Дополнительные сведения о кодах ошибок см. в разделе [_doserrno, код ошибки, _sys_errlist и _sys_nerr](../../c-runtime-library/errno-doserrno-sys-errlist-and-sys-nerr.md).

## <a name="remarks"></a>Комментарии

Каждая из этих функций копируется *`str`* в выходные данные *`stream`* в текущей позиции. **`fputws`** копирует аргумент расширенных символов *`str`* в *`stream`* как строку многобайтовых символов или строку расширенных символов в зависимости от того *`stream`* , открыт ли в текстовом режиме или в двоичном режиме соответственно. Ни одна из функций не копирует завершающий нуль-символ.

Эти две функции ведут себя одинаково, если поток открыт в режиме ANSI. **`fputs`** в настоящее время не поддерживает вывод в поток Юникода.

По умолчанию глобальное состояние этой функции ограничивается приложением. Чтобы изменить его, см. раздел [глобальное состояние в CRT](../global-state.md).

### <a name="generic-text-routine-mappings"></a>Сопоставления универсальных текстовых подпрограмм

|Подпрограмма TCHAR.H|_UNICODE и _MBCS не определены|_MBCS определено|_UNICODE определено|
|---------------------|------------------------------------|--------------------|-----------------------|
|**`_fputts`**|**`fputs`**|**`fputs`**|**`fputws`**|

## <a name="requirements"></a>Требования

|Компонент|Обязательный заголовок|
|--------------|---------------------|
|**`fputs`**|\<stdio.h>|
|**`fputws`**|\<stdio.h> либо \<wchar.h>|

Консоль не поддерживается в приложениях универсальная платформа Windows (UWP). Стандартные дескрипторы потока, связанные с консолью ( **`stdin`** , **`stdout`** и), **`stderr`** необходимо перенаправить, прежде чем функции среды выполнения C смогут использовать их в приложениях UWP. Дополнительные сведения о совместимости см. в разделе [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="example"></a>Пример

```C
// crt_fputs.c
// This program uses fputs to write
// a single line to the stdout stream.

#include <stdio.h>

int main( void )
{
   fputs( "Hello world from fputs.\n", stdout );
}
```

```Output
Hello world from fputs.
```

## <a name="see-also"></a>См. также раздел

[Потоковый ввод-вывод](../../c-runtime-library/stream-i-o.md)\
[`fgets`, `fgetws`](fgets-fgetws.md)\
[`gets`, `_getws`](../../c-runtime-library/gets-getws.md)\
[`puts`, `_putws`](puts-putws.md)
