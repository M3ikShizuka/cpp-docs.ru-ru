---
description: 'Дополнительные сведения: _msize_dbg'
title: _msize_dbg
ms.date: 11/04/2016
api_name:
- _msize_dbg
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
- _msize_dbg
- msize_dbg
helpviewer_keywords:
- memory blocks
- _msize_dbg function
- msize_dbg function
ms.assetid: a333f4b6-f8a2-4e61-bb69-cb34063b8cef
ms.openlocfilehash: 8ead0257e990322e88e20ce6111ff590dbc71686
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97256397"
---
# <a name="_msize_dbg"></a>_msize_dbg

Вычисляет размер блока памяти в куче (только в отладочной версии).

## <a name="syntax"></a>Синтаксис

```C
size_t _msize_dbg(
   void *userData,
   int blockType
);
```

### <a name="parameters"></a>Параметры

*userData*<br/>
Указатель на блок памяти, размер которого необходимо определить.

*blockType*<br/>
Тип указанного блока памяти: **_CLIENT_BLOCK** или **_NORMAL_BLOCK**.

## <a name="return-value"></a>Возвращаемое значение

При успешном завершении **_msize_dbg** возвращает размер указанного блока памяти (в байтах); в противном случае возвращается **значение NULL**.

## <a name="remarks"></a>Комментарии

**_msize_dbg** — это отладочная версия функции _ [MSize](msize.md) . Если [_DEBUG](../../c-runtime-library/debug.md) не определен, каждый вызов **_msize_dbg** сокращается до вызова **_msize**. И **_msize** , и **_msize_dbg** вычисляют размер блока памяти в базовой куче, но **_msize_dbg** добавляет две функции отладки: она включает буферы с любой стороны пользовательской части блока памяти в возвращенном размере и позволяет вычисление размера для конкретных типов блоков.

Сведения о выделении, инициализации и управлении блоками памяти в отладочной версии базовой кучи, см. в статье [CRT Debug Heap Details](/visualstudio/debugger/crt-debug-heap-details). Сведения о типах блоков выделения и их использовании см. в разделе [типы блоков в отладочной куче](/visualstudio/debugger/crt-debug-heap-details). Сведения о различиях между вызовом стандартной функции кучи и ее отладочной версии в сборке отладки приложения см. в разделе [Версии отладки функций выделения кучи](/visualstudio/debugger/debug-versions-of-heap-allocation-functions).

Эта функция проверяет свои параметры. Если *мемблокк* является пустым указателем, **_msize** вызывает обработчик недопустимого параметра, как описано в разделе [Проверка параметров](../../c-runtime-library/parameter-validation.md). Если ошибка обработана, **функция устанавливает значение** по **еинвал** и возвращает-1.

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|**_msize_dbg**|\<crtdbg.h>|

Дополнительные сведения о совместимости см. в разделе [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="libraries"></a>Библиотеки

Только отладочные версии [библиотек времени выполнения языка C](../../c-runtime-library/crt-library-features.md).

## <a name="example"></a>Пример

```C
// crt_msize_dbg.c
// compile with: /MTd
/*
* This program allocates a block of memory using _malloc_dbg
* and then calls _msize_dbg to display the size of that block.
* Next, it uses _realloc_dbg to expand the amount of
* memory used by the buffer and then calls _msize_dbg again to
* display the new amount of memory allocated to the buffer.
*/

#include <stdio.h>
#include <malloc.h>
#include <stdlib.h>
#include <crtdbg.h>

int main( void )
{
        long *buffer, *newbuffer;
        size_t size;

        /*
         * Call _malloc_dbg to include the filename and line number
         * of our allocation request in the header
         */
        buffer = (long *)_malloc_dbg( 40 * sizeof(long), _NORMAL_BLOCK, __FILE__, __LINE__ );
        if( buffer == NULL )
               exit( 1 );

        /*
         * Get the size of the buffer by calling _msize_dbg
         */
        size = _msize_dbg( buffer, _NORMAL_BLOCK );
        printf( "Size of block after _malloc_dbg of 40 longs: %u\n", size );

        /*
         * Reallocate the buffer using _realloc_dbg and show the new size
         */
        newbuffer = _realloc_dbg( buffer, size + (40 * sizeof(long)), _NORMAL_BLOCK, __FILE__, __LINE__ );
        if( newbuffer == NULL )
               exit( 1 );
        buffer = newbuffer;
        size = _msize_dbg( buffer, _NORMAL_BLOCK );
        printf( "Size of block after _realloc_dbg of 40 more longs: %u\n", size );

        free( buffer );
        exit( 0 );
}
```

### <a name="output"></a>Вывод

```Output
Size of block after _malloc_dbg of 40 longs: 160
Size of block after _realloc_dbg of 40 more longs: 320
```

## <a name="see-also"></a>См. также

[Отладочные подпрограммы](../../c-runtime-library/debug-routines.md)<br/>
[_malloc_dbg](malloc-dbg.md)<br/>
