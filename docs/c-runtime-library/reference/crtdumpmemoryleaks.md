---
description: 'Дополнительные сведения: _CrtDumpMemoryLeaks'
title: _CrtDumpMemoryLeaks
ms.date: 11/04/2016
api_name:
- _CrtDumpMemoryLeaks
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
- CRTDBG_LEAK_CHECK_DF
- CRTDBG_CHECK_CRT_DF
- _CRTDBG_LEAK_CHECK_DF
- CrtDumpMemoryLeaks
- _CrtDumpMemoryLeaks
- _CRTDBG_CHECK_CRT_DF
helpviewer_keywords:
- CrtDumpMemoryLeaks function
- CRTDBG_LEAK_CHECK_DF macro
- _CRTDBG_LEAK_CHECK_DF macro
- _CrtDumpMemoryLeaks function
- CRTDBG_CHECK_CRT_DF macro
- _CRTDBG_CHECK_CRT_DF macro
ms.assetid: 71b2eab4-7f55-44e8-a55a-bfea4f32d34c
ms.openlocfilehash: 83b3effdc4f3e8afdad24057ab55123aee924d60
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97319782"
---
# <a name="_crtdumpmemoryleaks"></a>_CrtDumpMemoryLeaks

Сбрасывает все блоки памяти в отладочной куче в случае утечки памяти (только в отладочной версии).

## <a name="syntax"></a>Синтаксис

```C

int _CrtDumpMemoryLeaks( void );
```

## <a name="return-value"></a>Возвращаемое значение

**_CrtDumpMemoryLeaks** возвращает значение true, если обнаружена утечка памяти. В противном случае функция возвращает значение FALSE.

## <a name="remarks"></a>Комментарии

Функция **_CrtDumpMemoryLeaks** определяет, произошла ли утечка памяти с момента запуска программы. При обнаружении утечки данные заголовка отладки для всех объектов в куче записываются в форме, которую пользователь может прочитать. Если [_DEBUG](../../c-runtime-library/debug.md) не определено, вызовы **_CrtDumpMemoryLeaks** удаляются во время предварительной обработки.

**_CrtDumpMemoryLeaks** часто вызывается в конце выполнения программы, чтобы убедиться, что вся память, выделенная приложением, была освобождена. Функция может вызываться автоматически при завершении программы путем включения **_CRTDBG_LEAK_CHECK_DF** битового поля флага [_crtDbgFlag](../../c-runtime-library/crtdbgflag.md) с помощью функции [_CrtSetDbgFlag](crtsetdbgflag.md) .

**_CrtDumpMemoryLeaks** вызывает [_CrtMemCheckpoint](crtmemcheckpoint.md) , чтобы получить текущее состояние кучи, а затем проверяет состояние блоков, которые не были освобождены. При обнаружении неосвобожденного блока **_CrtDumpMemoryLeaks** вызывает [_CrtMemDumpAllObjectsSince](crtmemdumpallobjectssince.md) для вывода сведений о всех объектах, выделенных в куче, с начала выполнения программы.

По умолчанию внутренние блоки времени выполнения C (**_CRT_BLOCK**) не включаются в операции дампа памяти. Функцию [_CrtSetDbgFlag](crtsetdbgflag.md) можно использовать, чтобы включить **_CRTDBG_CHECK_CRT_DF** бит **_crtDbgFlag** , чтобы включить эти блоки в процесс обнаружения утечек.

Дополнительные сведения о функциях состояния кучи и структуре **_CrtMemState** см. в разделе [функции создания отчетов о состоянии кучи](/visualstudio/debugger/crt-debug-heap-details). Дополнительные сведения о выделении, инициализации и управлении блоками памяти в отладочной версии основной кучи см. в разделе [CRT Debug Heap Details](/visualstudio/debugger/crt-debug-heap-details).

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|**_CrtDumpMemoryLeaks**|\<crtdbg.h>|

Дополнительные сведения о совместимости см. в разделе [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="libraries"></a>Библиотеки

Только отладочные версии [библиотек времени выполнения языка C](../../c-runtime-library/crt-library-features.md).

## <a name="example"></a>Пример

Пример использования **_CrtDumpMemoryLeaks** см. в разделе [crt_dbg1](https://github.com/Microsoft/VCSamples/tree/master/VC2010Samples/crt/crt_dbg1).

## <a name="see-also"></a>См. также раздел

[Отладочные подпрограммы](../../c-runtime-library/debug-routines.md)<br/>
