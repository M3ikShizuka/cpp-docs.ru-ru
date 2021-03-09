---
title: _CrtMemDifference
description: 'Дополнительные сведения: _CrtMemDifference'
ms.date: 3/8/2021
api_name:
- _CrtMemDifference
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
- _CrtMemDifference
- CrtMemDifference
helpviewer_keywords:
- CrtMemDifference function
- _CrtMemDifference function
ms.openlocfilehash: 9a6a213df867f98bfb921abd940ba23297c5ffef
ms.sourcegitcommit: 90c300b74f6556cb5d989802d2e80d79542f55e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "102514607"
---
# `_CrtMemDifference`

Сравнивает два состояния памяти и возвращает их различия (только отладочная версия).

## <a name="syntax"></a>Синтаксис

```C
int _CrtMemDifference(
   _CrtMemState *stateDiff,
   const _CrtMemState *oldState,
   const _CrtMemState *newState
);
```

### <a name="parameters"></a>Параметры

*`stateDiff`*\
Указатель на **`_CrtMemState`** структуру, используемую для хранения различий между двумя состояниями памяти (возвращаемые).

*`oldState`*\
Указатель на более раннее состояние памяти ( **`_CrtMemState`** структура).

*`newState`*\
Указатель на более позднее состояние памяти ( **`_CrtMemState`** структура).

## <a name="return-value"></a>Возвращаемое значение

Если состояния памяти значительно отличаются, **`_CrtMemDifference`** возвращает `TRUE` . В противном случае функция возвращает значение FALSE.

## <a name="remarks"></a>Комментарии

**`_CrtMemDifference`** Функция сравнивает *`oldState`* и *`newState`* сохраняет свои различия в *`stateDiff`* , которые затем могут использоваться приложением для обнаружения утечек памяти и других проблем с памятью. Если [_DEBUG](../../c-runtime-library/debug.md) не определена, вызовы **`_CrtMemDifference`** удаляются во время предварительной обработки.

*`newState`* и *`oldState`* должны быть допустимыми указателями на **`_CrtMemState`** структуру, определенную в файле Crtdbg. h, которая была заполнена [`_CrtMemCheckpoint`](crtmemcheckpoint.md) до вызова метода **`_CrtMemDifference`** . *`stateDiff`* должен быть указателем на ранее выделенный экземпляр **`_CrtMemState`** структуры. Если параметр *`stateDiff`* , *`newState`* или *`oldState`* имеет значение **`NULL`** , вызывается обработчик недопустимых параметров, как описано в разделе [Проверка параметров](../../c-runtime-library/parameter-validation.md). Если выполнение может быть продолжено, [`errno, _doserrno, _sys_errlist, and _sys_nerr`](../../c-runtime-library/errno-doserrno-sys-errlist-and-sys-nerr.md) для задается значение **`EINVAL`** , а функция возвращает значение false.

**`_CrtMemDifference`** Сравнивает **`_CrtMemState`** значения полей блоков в *`oldState`* *`newState`* и сохраняет результат в *`stateDiff`* . Если количество выделенных типов блоков или общее количество выделенных блоков каждого типа различается в двух состояниях памяти, считается, что состояния значительно отличаются. Разница между наибольшим объемом, когда-либо выделено за один раз для двух состояний, и разность между общими выделениями для двух состояний также хранится в *`stateDiff`* .

По умолчанию внутренние блоки времени выполнения C ( **`_CRT_BLOCK`** ) не включаются в операции состояния памяти. Функцию [_CrtSetDbgFlag](crtsetdbgflag.md) можно использовать, чтобы включить **`_CRTDBG_CHECK_CRT_DF`** бит **`_crtDbgFlag`** для включения этих блоков в обнаружение утечек и другие операции состояния памяти. Освобождение блоков памяти ( **`_FREE_BLOCK`** ) не приводит **`_CrtMemDifference`** к возврату `TRUE` .

Дополнительные сведения о функциях состояния кучи и **`_CrtMemState`** структуре см. в [разделе функции создания отчетов о состоянии кучи](/visualstudio/debugger/crt-debug-heap-details). Сведения о выделении, инициализации и управлении блоками памяти в отладочной версии базовой кучи, см. в статье [CRT Debug Heap Details](/visualstudio/debugger/crt-debug-heap-details).

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|Необязательный заголовок|
|-------------|---------------------|---------------------|
|**`_CrtMemDifference`**|`<crtdbg.h>`|`<errno.h>`|

Дополнительные сведения о совместимости см. в разделе [Compatibility](../../c-runtime-library/compatibility.md).

**Библиотеки:** Отладочные версии [библиотек времени выполнения C](../../c-runtime-library/crt-library-features.md) .

## <a name="see-also"></a>См. также

[Отладочные подпрограммы](../../c-runtime-library/debug-routines.md)\
[`_crtDbgFlag`](../../c-runtime-library/crtdbgflag.md)\
