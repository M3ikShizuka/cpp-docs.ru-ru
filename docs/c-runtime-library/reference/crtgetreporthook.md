---
description: 'Дополнительные сведения: _CrtGetReportHook'
title: _CrtGetReportHook
ms.date: 11/04/2016
api_name:
- _CrtGetReportHook
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
- CrtGetReportHook
- _CrtGetReportHook
helpviewer_keywords:
- CrtGetReportHook function
- _CrtGetReportHook function
ms.assetid: 922758ed-7edd-4359-9c92-0535192dc11a
ms.openlocfilehash: 9c950341e3f1b0231620449d983fcfe5bc0f5f12
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97319743"
---
# <a name="_crtgetreporthook"></a>_CrtGetReportHook

Извлекает определяемую клиентом функцию отчетов путем ее прикрепления к процессу создания отчетов среды выполнения языка C (только в отладочной версии).

## <a name="syntax"></a>Синтаксис

```C
_CRT_REPORT_HOOK _CrtGetReportHook( void );
```

## <a name="return-value"></a>Возвращаемое значение

Возвращает текущую определяемую клиентом функцию отчетов.

## <a name="remarks"></a>Комментарии

**_CrtGetReportHook** позволяет приложению получить текущую функцию отчетов для процесса создания отчетов отладочной библиотеки времени выполнения C.

Дополнительные сведения о других допускающих подключение функциях среды выполнения и написании собственных определяемых клиентом функциях-ловушках см. в разделе [Написание функций отладочных ловушек](/visualstudio/debugger/debug-hook-function-writing).

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|**_CrtGetReportHook**|\<crtdbg.h>|

Дополнительные сведения о совместимости см. в разделе [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="libraries"></a>Библиотеки

Только отладочные версии [библиотек времени выполнения языка C](../../c-runtime-library/crt-library-features.md).

## <a name="example"></a>Пример

Пример использования **_CrtSetReportHook** см. в разделе [отчет](https://github.com/Microsoft/VCSamples/tree/master/VC2010Samples/crt/report).

## <a name="see-also"></a>См. также раздел

[Отладочные подпрограммы](../../c-runtime-library/debug-routines.md)<br/>
[_CrtSetReportHook](crtsetreporthook.md)<br/>
