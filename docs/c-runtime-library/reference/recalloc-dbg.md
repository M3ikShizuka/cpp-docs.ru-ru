---
description: 'Дополнительные сведения: _recalloc_dbg'
title: _recalloc_dbg
ms.date: 11/04/2016
api_name:
- _recalloc_dbg
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
- recalloc_dbg
- _recalloc_dbg
helpviewer_keywords:
- _recalloc_dbg function
- recalloc_dbg function
ms.assetid: 43c3e9b2-be6d-4508-9b0f-3220c8a47ca3
ms.openlocfilehash: abad8ff877a78bc589a48da689766322ad8438de
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97254265"
---
# <a name="_recalloc_dbg"></a>_recalloc_dbg

Повторно выделяет массив и инициализирует его элементы нулями (только отладочная версия).

## <a name="syntax"></a>Синтаксис

```C
void *_recalloc_dbg(
   void *userData,
   size_t num,
   size_t size,
   int blockType,
   const char *filename,
   int linenumber
);
```

### <a name="parameters"></a>Параметры

*userData*<br/>
Указатель на ранее выделенный блок памяти.

*number*<br/>
Запрошенное число блоков памяти.

*size*<br/>
Запрошенный размер каждого блока памяти (байт).

*blockType*<br/>
Запрошенный тип блока памяти: **_CLIENT_BLOCK** или **_NORMAL_BLOCK**.

Сведения о типах блоков выделения и их использовании см. в разделе [типы блоков в отладочной куче](/visualstudio/debugger/crt-debug-heap-details).

*filename*<br/>
Указатель на имя исходного файла, который запросил операцию выделения, или **значение NULL**.

*LineNumber*<br/>
Номер строки в исходном файле, где была запрошена операция выделения, или **значение NULL**.

Параметры *filename* и *LineNumber* доступны только при явном вызове **_recalloc_dbg** или при определении константы препроцессора [_CRTDBG_MAP_ALLOC](../../c-runtime-library/crtdbg-map-alloc.md) .

## <a name="return-value"></a>Возвращаемое значение

При успешном завершении эта функция либо возвращает указатель на пользовательскую часть перераспределенного блока памяти, вызывает новую функцию обработчика, либо возвращает **значение NULL**. Полное описание поведения возвращения см. в следующем разделе "Примечания". Дополнительные сведения о том, как используется новая функция обработчика, см. в описании функции [_recalloc](recalloc.md).

## <a name="remarks"></a>Комментарии

**_recalloc_dbg** — это отладочная версия функции [_recalloc](recalloc.md) . Если [_DEBUG](../../c-runtime-library/debug.md) не определен, каждый вызов **_recalloc_dbg** сокращается до вызова **_recalloc**. Как **_recalloc** , так и **_recalloc_dbg** перераспределяют блок памяти в базовой куче, но **_recalloc_dbg** поддерживает несколько отладочных функций: буферы на обеих сторонах пользовательской части блока для проверки утечек, параметр типа блока для трассировки определенных типов выделения и сведения *filename* / *LineNumber* для определения источника запросов на выделение.

**_recalloc_dbg** перераспределяет указанный блок памяти с немного больше пространства, чем запрошенный размер (размер *номера*  *  ), который может быть больше или меньше размера первоначально выделенного блока памяти. Дополнительное пространство используется диспетчером кучи отладки, чтобы связать блоки памяти отладки и предоставить приложению сведения о заголовке отладки и буферы перезаписи. Перераспределение может привести к перемещению исходного блока памяти в другое расположение в куче, а также к изменению размера блока памяти. Пользовательская часть блока заполняется значением 0xCD, а все буферы перезаписи — значением 0xFD.

**_recalloc_dbg** устанавливает **значение** **еномем** , если выделение памяти завершается ошибкой; **Еинвал** возвращается, если объем необходимой памяти (включая ранее накладные расходы) превышает **_HEAP_MAXREQ**. Дополнительные сведения об этих и других кодах ошибок см. в разделе [errno, _doserrno, _sys_errlist и _sys_nerr](../../c-runtime-library/errno-doserrno-sys-errlist-and-sys-nerr.md).

Сведения о выделении, инициализации и управлении блоками памяти в отладочной версии базовой кучи, см. в статье [CRT Debug Heap Details](/visualstudio/debugger/crt-debug-heap-details). Сведения о различиях между вызовом стандартной функции кучи и ее отладочной версии в сборке отладки приложения см. в разделе [Версии отладки функций выделения кучи](/visualstudio/debugger/debug-versions-of-heap-allocation-functions).

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|**_recalloc_dbg**|\<crtdbg.h>|

Дополнительные сведения о совместимости см. в разделе [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="libraries"></a>Библиотеки

Только отладочные версии [библиотек времени выполнения языка C](../../c-runtime-library/crt-library-features.md).

## <a name="see-also"></a>См. также раздел

[Отладочные подпрограммы](../../c-runtime-library/debug-routines.md)<br/>
