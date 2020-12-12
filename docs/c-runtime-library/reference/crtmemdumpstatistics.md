---
description: 'Дополнительные сведения: _CrtMemDumpStatistics'
title: _CrtMemDumpStatistics
ms.date: 11/04/2016
api_name:
- _CrtMemDumpStatistics
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
- CrtMemDumpStatistics
- _CrtMemDumpStatistics
helpviewer_keywords:
- _CrtMemDumpStatistics function
- CrtMemDumpStatistics function
ms.assetid: 27b9d731-3184-4a2d-b9a7-6566ab28a9fe
ms.openlocfilehash: 2f02c35ff61dc2bc5ac7e8dfbe921fa48731c2b3
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97319620"
---
# <a name="_crtmemdumpstatistics"></a>_CrtMemDumpStatistics

Помещает в дамп данные заголовка отладки для указанного состояния кучи в понятной пользователю форме (только отладочная версия).

## <a name="syntax"></a>Синтаксис

```C
void _CrtMemDumpStatistics(
   const _CrtMemState *state
);
```

### <a name="parameters"></a>Параметры

*state*<br/>
Указатель на состояние кучи для создания дампа.

## <a name="remarks"></a>Комментарии

Функция **_CrtMemDumpStatistics** выводит данные заголовка отладки для указанного состояния кучи в форме, доступной для чтения пользователем. Статистика дампа может использоваться приложением для отслеживания операций выделения памяти и выявления проблем с памятью. Состояние памяти может содержать состояние определенной кучи или разницу между двумя состояниями. Если [_DEBUG](../../c-runtime-library/debug.md) не определено, вызовы **_CrtMemDumpStatistics** удаляются во время предварительной обработки.

Параметр *State* должен быть указателем на структуру **_CrtMemState** , которая была заполнена [_CrtMemCheckpoint](crtmemcheckpoint.md) или возвращена [_CrtMemDifference](crtmemdifference.md) перед вызовом **_CrtMemDumpStatistics** . Если параметр *State* имеет **значение NULL**, вызывается обработчик недопустимых параметров, как описано в разделе [Проверка параметров](../../c-runtime-library/parameter-validation.md). Если выполнение может быть продолжено **, для** параметра **еинвал** задается значение, а никакие действия не выполняются. Дополнительные сведения см. в разделе [errno, _doserrno, _sys_errlist и _sys_nerr](../../c-runtime-library/errno-doserrno-sys-errlist-and-sys-nerr.md).

Дополнительные сведения о функциях состояния кучи и структуре **_CrtMemState** см. в разделе [функции создания отчетов о состоянии кучи](/visualstudio/debugger/crt-debug-heap-details). Дополнительные сведения о выделении, инициализации и управлении блоками памяти в отладочной версии основной кучи см. в разделе [CRT Debug Heap Details](/visualstudio/debugger/crt-debug-heap-details).

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|Необязательные заголовки|
|-------------|---------------------|----------------------|
|**_CrtMemDumpStatistics**|\<crtdbg.h>|\<errno.h>|

Дополнительные сведения о совместимости см. в разделе [Compatibility](../../c-runtime-library/compatibility.md).

**Библиотеки:** только отладочные версии [функций библиотеки CRT](../../c-runtime-library/crt-library-features.md).

## <a name="see-also"></a>См. также раздел

[Отладочные подпрограммы](../../c-runtime-library/debug-routines.md)<br/>
