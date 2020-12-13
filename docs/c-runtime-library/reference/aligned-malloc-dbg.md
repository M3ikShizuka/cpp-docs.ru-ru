---
description: 'Дополнительные сведения: _aligned_malloc_dbg'
title: _aligned_malloc_dbg
ms.date: 11/04/2016
api_name:
- _aligned_malloc_dbg
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
- _aligned_malloc_dbg
- aligned_malloc_dbg
helpviewer_keywords:
- aligned_malloc_dbg function
- _aligned_malloc_dbg function
ms.assetid: fb0429c3-685d-4826-9075-2515c5bdc5c6
ms.openlocfilehash: dc593ee827bb5e3453695c5e35816116854d0460
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97334271"
---
# <a name="_aligned_malloc_dbg"></a>_aligned_malloc_dbg

Выделяет память в указанных границах выравнивания с дополнительным пространством для заголовка отладки и буферов перезаписи (только отладочная версия).

## <a name="syntax"></a>Синтаксис

```C
void * _aligned_malloc_dbg(
    size_t size,
    size_t alignment,
   const char *filename,
   int linenumber
);
```

### <a name="parameters"></a>Параметры

*size*<br/>
Размер запрошенного выделения памяти.

*Выравнивание*<br/>
Значение выравнивания, которое должно быть целой степенью числа 2.

*filename*<br/>
Указатель на имя исходного файла, который запросил операцию выделения, или NULL.

*LineNumber*<br/>
Номер строки в исходном файле, в которой была запрошена операция выделения, или NULL.

## <a name="return-value"></a>Возвращаемое значение

Указатель на блок памяти, который был выделен, или значение NULL, если операция завершилась ошибкой.

## <a name="remarks"></a>Комментарии

**_aligned_malloc_dbg** — это отладочная версия функции [_aligned_malloc](aligned-malloc.md) . Если [_DEBUG](../../c-runtime-library/debug.md) не определен, каждый вызов **_aligned_malloc_dbg** уменьшается до вызова `_aligned_malloc` . `_aligned_malloc`И, и **_aligned_malloc_dbg** выделить блок памяти в базовой куче, но **_aligned_malloc_dbg** предлагает несколько функций отладки: буферы с обеих сторон пользовательской части блока для проверки на наличие утечек и сведения *filename* / *LineNumber* для определения источника запросов на выделение. Отслеживание конкретных типов выделения с помощью параметра типа блока не является поддерживаемой функцией отладки для согласованных выделений. Выделенные выделения будут отображаться как тип блока _NORMAL_BLOCK.

**_aligned_malloc_dbg** выделяет блок памяти с немного больше пространства, чем запрошенный *Размер*. Дополнительное пространство используется диспетчером кучи отладки, чтобы связать блоки памяти отладки и предоставить приложению сведения о заголовке отладки и буферы перезаписи. При выделении блока пользовательская часть блока заполняется значением 0xCD, а все буферы перезаписи — значением 0xFD.

**_aligned_malloc_dbg** задает `errno` значение, `ENOMEM` Если выделение памяти завершается ошибкой или если необходимый объем памяти (включая ранее загруженные издержки) превышает `_HEAP_MAXREQ` . Дополнительные сведения об этих и других кодах ошибок см. в разделе [errno, _doserrno, _sys_errlist и _sys_nerr](../../c-runtime-library/errno-doserrno-sys-errlist-and-sys-nerr.md). Кроме того, **_aligned_malloc_dbg** проверяет свои параметры. Если значение *alignment* не равно 2 или *size* равно нулю, эта функция вызывает обработчик недопустимых параметров, как описано в разделе [Проверка параметров](../../c-runtime-library/parameter-validation.md). Если выполнение может быть продолжено, эта функция возвращает значение NULL и задает `errno` для значение `EINVAL` .

Сведения о выделении, инициализации и управлении блоками памяти в отладочной версии базовой кучи, см. в статье [CRT Debug Heap Details](/visualstudio/debugger/crt-debug-heap-details). Сведения о типах блоков выделения и их использовании см. в разделе [типы блоков в отладочной куче](/visualstudio/debugger/crt-debug-heap-details). Сведения о различиях между вызовом стандартной функции кучи и ее отладочной версии в сборке отладки приложения см. в разделе [Версии отладки функций выделения кучи](/visualstudio/debugger/debug-versions-of-heap-allocation-functions).

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|**_aligned_malloc_dbg**|\<crtdbg.h>|

Дополнительные сведения о совместимости см. в разделе [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="libraries"></a>Библиотеки

Только отладочные версии [библиотек времени выполнения языка C](../../c-runtime-library/crt-library-features.md).

## <a name="see-also"></a>См. также раздел

[Отладочные подпрограммы](../../c-runtime-library/debug-routines.md)
