---
description: 'Дополнительные сведения о: memmove, wmemmove'
title: memmove, wmemmove
ms.date: 1/14/2021
api_name:
- memmove
- wmemmove
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
- ntoskrnl.exe
- api-ms-win-crt-private-l1-1-0.dll
api_type:
- DLLExport
topic_type:
- apiref
f1_keywords:
- memmove
- wmemmove
helpviewer_keywords:
- wmemmove function
- memmove function
ms.openlocfilehash: 6f9942c232710585aa5837510f0f04e5db36fb2a
ms.sourcegitcommit: 1cd8f8a75fd036ffa57bc70f3ca869042d8019d4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "98243129"
---
# <a name="memmove-wmemmove"></a>`memmove`, `wmemmove`

Перемещает один буфер в другой. Доступны более безопасные версии этих функций; см. раздел [ `memmove_s` , `wmemmove_s` ](memmove-s-wmemmove-s.md).

## <a name="syntax"></a>Синтаксис

```C
void *memmove(
   void *dest,
   const void *src,
   size_t count
);
wchar_t *wmemmove(
   wchar_t *dest,
   const wchar_t *src,
   size_t count
);
```

### <a name="parameters"></a>Параметры

*`dest`*\
Конечный объект.

*`src`*\
Исходный объект.

*`count`*\
Число байтов ( **`memmove`** ) или символов ( **`wmemmove`** ) для копирования.

## <a name="return-value"></a>Возвращаемое значение

Значение *`dest`* .

## <a name="remarks"></a>Комментарии

Копирует *`count`* байты ( **`memmove`** ) или символы ( **`wmemmove`** ) из *`src`* в *`dest`* . Если отдельные области конечного объекта перекрывают области исходного объекта, то обе эти функции гарантируют, что байты исходного объекта в перекрывающейся области будут скопированы, прежде чем будут перезаписаны.

**Примечание о безопасности**. Убедитесь в том, что буфер назначения равен или превосходит по размеру исходный буфер. Дополнительные сведения см. в разделе [Как избежать переполнения буфера](/windows/win32/SecBP/avoiding-buffer-overruns).

**`memmove`** Функции и **`wmemmove`** будут считаться устаревшими только в том случае, если константа **`_CRT_SECURE_DEPRECATE_MEMORY`** определена до оператора включения, чтобы функции были устаревшими, например, в примере ниже:

```C
#define _CRT_SECURE_DEPRECATE_MEMORY
#include <string.h>
```

или

```C
#define _CRT_SECURE_DEPRECATE_MEMORY
#include <wchar.h>
```

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|**`memmove`**|`<string.h>`|
|**`wmemmove`**|`<wchar.h>`|

Дополнительные сведения о совместимости см. в разделе [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="example"></a>Пример

```C
// crt_memcpy.c
// Illustrate overlapping copy: memmove
// always handles it correctly; memcpy may handle
// it correctly.
//

#include <memory.h>
#include <string.h>
#include <stdio.h>

char str1[7] = "aabbcc";

int main( void )
{
   printf( "The string: %s\n", str1 );
   memcpy( str1 + 2, str1, 4 );
   printf( "New string: %s\n", str1 );

   strcpy_s( str1, sizeof(str1), "aabbcc" );   // reset string

   printf( "The string: %s\n", str1 );
   memmove( str1 + 2, str1, 4 );
   printf( "New string: %s\n", str1 );
}
```

```Output
The string: aabbcc
New string: aaaabb
The string: aabbcc
New string: aaaabb
```

## <a name="see-also"></a>См. также

[Обработка буфера](../../c-runtime-library/buffer-manipulation.md)\
[`_memccpy`](memccpy.md)\
[`memcpy`, `wmemcpy`](memcpy-wmemcpy.md)\
[`strcpy`, `wcscpy`, `_mbscpy`](strcpy-wcscpy-mbscpy.md)\
[`strncpy`, `_strncpy_l`, `wcsncpy`, `_wcsncpy_l`, `_mbsncpy`, `_mbsncpy_l`](strncpy-strncpy-l-wcsncpy-wcsncpy-l-mbsncpy-mbsncpy-l.md)\
