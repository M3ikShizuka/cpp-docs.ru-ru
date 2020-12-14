---
description: 'Дополнительные сведения: _memccpy'
title: _memccpy
ms.date: 11/04/2016
api_name:
- _memccpy
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
- api-ms-win-crt-string-l1-1-0.dll
api_type:
- DLLExport
topic_type:
- apiref
f1_keywords:
- _memccpy
helpviewer_keywords:
- _memccpy function
- memccpy function
ms.assetid: 9a2337df-6e85-4eba-b247-dd0532f45ddb
ms.openlocfilehash: f3cbfbd1e112c724d6223a6c6d28f0915dcd7ca0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97240095"
---
# <a name="_memccpy"></a>_memccpy

Копирует символы из буфера.

## <a name="syntax"></a>Синтаксис

```C
void *_memccpy(
   void *dest,
   const void *src,
   int c,
   size_t count
);
```

### <a name="parameters"></a>Параметры

*dest*<br/>
Указатель на назначение.

*src*<br/>
Указатель на источник.

*c*<br/>
Последний символ для копирования.

*count*<br/>
Число символов.

## <a name="return-value"></a>Возвращаемое значение

Если копируется символ *c* , **_memccpy** возвращает указатель на символ в *dest* , который сразу же следует за символом. Если *c* не копируется, возвращается **значение NULL**.

## <a name="remarks"></a>Комментарии

Функция **_memccpy** копирует 0 или более символов из *src* в *dest*, прекращает выполнение при копировании символа *c* или при копировании *количества* символов (в зависимости от того, что происходит раньше).

**Примечание о безопасности**. Убедитесь в том, что буфер назначения равен или превосходит по размеру исходный буфер. Дополнительные сведения см. в разделе [Как избежать переполнения буфера](/windows/win32/SecBP/avoiding-buffer-overruns).

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|**_memccpy**|\<memory.h> или \<string.h>|

Дополнительные сведения о совместимости см. в разделе [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="libraries"></a>Библиотеки

Все версии [библиотек времени выполнения языка C](../../c-runtime-library/crt-library-features.md).

## <a name="example"></a>Пример

```C
// crt_memccpy.c

#include <memory.h>
#include <stdio.h>
#include <string.h>

char string1[60] = "The quick brown dog jumps over the lazy fox";

int main( void )
{
   char buffer[61];
   char *pdest;

   printf( "Function: _memccpy 60 characters or to character 's'\n" );
   printf( "Source: %s\n", string1 );
   pdest = _memccpy( buffer, string1, 's', 60 );
   *pdest = '\0';
   printf( "Result: %s\n", buffer );
   printf( "Length: %d characters\n", strlen( buffer ) );
}
```

### <a name="output"></a>Вывод

```Output
Function: _memccpy 60 characters or to character 's'
Source: The quick brown dog jumps over the lazy fox
Result: The quick brown dog jumps
Length: 25 characters
```

## <a name="see-also"></a>См. также

[Обработка буфера](../../c-runtime-library/buffer-manipulation.md)<br/>
[memchr, wmemchr](memchr-wmemchr.md)<br/>
[memcmp, wmemcmp](memcmp-wmemcmp.md)<br/>
[memcpy, wmemcpy](memcpy-wmemcpy.md)<br/>
[memset, wmemset](memset-wmemset.md)<br/>
