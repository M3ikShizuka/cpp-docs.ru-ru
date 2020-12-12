---
description: 'Дополнительные сведения: _CrtSetBreakAlloc'
title: _CrtSetBreakAlloc
ms.date: 11/04/2016
api_name:
- _CrtSetBreakAlloc
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
- CrtSetBreakAlloc
- _CrtSetBreakAlloc
helpviewer_keywords:
- CrtSetBreakAlloc function
- _CrtSetBreakAlloc function
ms.assetid: 33bfc6af-a9ea-405b-a29f-1c2d4d9880a1
ms.openlocfilehash: 07db47aa23fe95e86b3341813137643b81f57fbc
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97319603"
---
# <a name="_crtsetbreakalloc"></a>_CrtSetBreakAlloc

Задает точку останова для указанного порядкового номера выделения объекта (только отладочная версия).

## <a name="syntax"></a>Синтаксис

```C
long _CrtSetBreakAlloc(
   long lBreakAlloc
);
```

### <a name="parameters"></a>Параметры

*lBreakAlloc*<br/>
Порядковый номер выделения, для которого задается точка останова.

## <a name="return-value"></a>Возвращаемое значение

Возвращает предыдущий порядковый номер выделения объекта, для которого задана точка останова.

## <a name="remarks"></a>Комментарии

**_CrtSetBreakAlloc** позволяет приложению выполнять обнаружение утечек памяти, нарушая заданную точку выделения памяти и отменив трассировку на источник запроса. Функция использует последовательный порядковый номер выделения объекта, назначенный блоку памяти во время выделения в куче. Если [_DEBUG](../../c-runtime-library/debug.md) не определено, вызовы **_CrtSetBreakAlloc** удаляются во время предварительной обработки.

Порядковый номер выделения объекта хранится в поле *lRequest* структуры **_CrtMemBlockHeader**, определенной в Crtdbg.h. Если сведения о блоке памяти передаются одной из функций отладочного дампа, это значение заключается в фигурные скобки, например {36} .

Дополнительные сведения о том, как **_CrtSetBreakAlloc** можно использовать с другими функциями управления памятью, см. в разделе [Отслеживание запросов на выделение кучи](/visualstudio/debugger/crt-debug-heap-details). Дополнительные сведения о выделении, инициализации и управлении блоками памяти в отладочной версии основной кучи см. в разделе [CRT Debug Heap Details](/visualstudio/debugger/crt-debug-heap-details).

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|**_CrtSetBreakAlloc**|\<crtdbg.h>|

Дополнительные сведения о совместимости см. в разделе [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="libraries"></a>Библиотеки

Только отладочные версии [библиотек времени выполнения языка C](../../c-runtime-library/crt-library-features.md).

## <a name="example"></a>Пример

```C
// crt_setbrkal.c
// compile with: -D_DEBUG /MTd -Od -Zi -W3 /c /link -verbose:lib -debug

/*
* In this program, a call is made to the _CrtSetBreakAlloc routine
* to verify that the debugger halts program execution when it reaches
* a specified allocation number.
*/

#include <malloc.h>
#include <crtdbg.h>

int main( )
{
        long allocReqNum;
        char *my_pointer;

        /*
         * Allocate "my_pointer" for the first
         * time and ensure that it gets allocated correctly
         */
        my_pointer = malloc(10);
        _CrtIsMemoryBlock(my_pointer, 10, &allocReqNum, NULL, NULL);

        /*
         * Set a breakpoint on the allocation request
         * number for "my_pointer"
         */
        _CrtSetBreakAlloc(allocReqNum+2);

        /*
         * Alternate freeing and reallocating "my_pointer"
         * to verify that the debugger halts program execution
         * when it reaches the allocation request
         */
        free(my_pointer);
        my_pointer = malloc(10);
        free(my_pointer);
        my_pointer = malloc(10);
        free(my_pointer);
}
```

## <a name="see-also"></a>См. также раздел

[Отладочные подпрограммы](../../c-runtime-library/debug-routines.md)<br/>
