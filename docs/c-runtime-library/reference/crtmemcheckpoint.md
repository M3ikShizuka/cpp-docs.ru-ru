---
description: 'Дополнительные сведения: _CrtMemCheckpoint'
title: _CrtMemCheckpoint
ms.date: 11/04/2016
api_name:
- _CrtMemCheckpoint
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
- CrtMemCheckpoint
- _CrtMemCheckpoint
- crtdbg/_CrtMemCheckpoint
helpviewer_keywords:
- CrtMemCheckpoint function
- _CrtMemCheckpoint function
ms.assetid: f1bacbaa-5a0c-498a-ac7a-b6131d83dfbc
ms.openlocfilehash: f7a88e63c99c063999f3de0d01e019fecd10496f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97319681"
---
# <a name="_crtmemcheckpoint"></a>_CrtMemCheckpoint

Получает текущее состояние отладочной кучи и сохраняет его в предоставленной приложением структуре **_CrtMemState** (только отладочная версия).

## <a name="syntax"></a>Синтаксис

```C
void _CrtMemCheckpoint(
   _CrtMemState *state
);
```

### <a name="parameters"></a>Параметры

*state*<br/>
Указатель на структуру **_CrtMemState** для заполнения контрольной точкой памяти.

## <a name="remarks"></a>Комментарии

Функция **_CrtMemCheckpoint** создает моментальный снимок текущего состояния отладочной кучи в любое заданное время. Этот моментальный снимок могут использовать другие функции управления состоянием кучи, такие как [_CrtMemDifference](crtmemdifference.md) , для обнаружения утечек памяти и других проблем. Если [_DEBUG](../../c-runtime-library/debug.md) не определено, вызовы **_CrtMemState** удаляются во время предварительной обработки.

Приложение должно передать указатель на ранее выделенный экземпляр структуры **_CrtMemState** , определенный в файле Crtdbg. h в параметре *State* . Если **_CrtMemCheckpoint** обнаруживает ошибку во время создания контрольной точки, функция создает **_CRT_WARNный** отчет об отладке, описывающий проблему.

Дополнительные сведения о функциях состояния кучи и структуре **_CrtMemState** см. в разделе [функции создания отчетов о состоянии кучи](/visualstudio/debugger/crt-debug-heap-details). Дополнительные сведения о выделении, инициализации и управлении блоками памяти в отладочной версии основной кучи см. в разделе [CRT Debug Heap Details](/visualstudio/debugger/crt-debug-heap-details).

Если параметр *State* имеет **значение NULL**, вызывается обработчик недопустимых параметров, как описано в разделе [Проверка параметров](../../c-runtime-library/parameter-validation.md). Если выполнение может быть продолжено, в параметре "_doserrno", " [_sys_errlist" и _sys_nerr](../../c-runtime-library/errno-doserrno-sys-errlist-and-sys-nerr.md) задано значение " **еинвал** ", а функция возвращает.

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|**_CrtMemCheckpoint**|\<crtdbg.h>, \<errno.h>|

Дополнительные сведения о совместимости см. в разделе [Compatibility](../../c-runtime-library/compatibility.md).

**Библиотеки:** только отладочные версии UCRT.

## <a name="see-also"></a>См. также раздел

[Отладочные подпрограммы](../../c-runtime-library/debug-routines.md)<br/>
[_CrtMemDifference](crtmemdifference.md)<br/>
