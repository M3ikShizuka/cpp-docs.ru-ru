---
description: 'Дополнительные сведения: _CrtSetReportHook'
title: _CrtSetReportHook
ms.date: 11/04/2016
api_name:
- _CrtSetReportHook
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
- _CrtSetReportHook
- CrtSetReportHook
helpviewer_keywords:
- CrtSetReportHook function
- _CrtSetReportHook function
ms.assetid: 1ae7c64f-8c84-4797-9574-b59f00f7a509
ms.openlocfilehash: 1e99e17b3a245dfe78e5a0f7367e422f4dc97600
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97342248"
---
# <a name="_crtsetreporthook"></a>_CrtSetReportHook

Устанавливает определяемую клиентом функцию отчетов путем ее прикрепления к процессу создания отчетов среды выполнения языка C (только отладочная версия).

## <a name="syntax"></a>Синтаксис

```C
_CRT_REPORT_HOOK _CrtSetReportHook(
   _CRT_REPORT_HOOK reportHook
);
```

### <a name="parameters"></a>Параметры

*репорсук*<br/>
Новая определяемая клиентом функция отчетов, которую необходимо прикрепить к процессу создания отчетов среды выполнения языка C.

## <a name="return-value"></a>Возвращаемое значение

Возвращает предыдущую определяемую клиентом функцию отчетов.

## <a name="remarks"></a>Комментарии

**_CrtSetReportHook** позволяет приложению использовать собственную функцию отчетов в процессе создания отчетов отладочной библиотеки времени выполнения C. В результате всякий раз, когда для создания отчета отладки вызывается функция [_CrtDbgReport](crtdbgreport-crtdbgreportw.md), сначала вызывается функция отчетов приложения. Эта функция позволяет приложению выполнять такие операции, как фильтрация отладочных отчетов, чтобы можно было сосредоточиться на определенных типах выделения или отправить отчет в назначения, недоступные с помощью **_CrtDbgReport**. Если [_DEBUG](../../c-runtime-library/debug.md) не определено, вызовы **_CrtSetReportHook** удаляются во время предварительной обработки.

Более надежную версию **_CrtSetReportHook** см. в разделе [_CrtSetReportHook2](crtsetreporthook2-crtsetreporthookw2.md).

Функция **_CrtSetReportHook** устанавливает новую определяемую клиентом функцию отчетов, указанную в *репорсук* , и возвращает предыдущий клиентский обработчик. В следующем примере показано, как должен быть объявлен прототип определяемого клиентом обработчика отчетов:

```C
int YourReportHook( int reportType, char *message, int *returnValue );
```

где *reportType* — это тип отладочного отчета (**_CRT_WARN**, **_CRT_ERROR** или **_CRT_ASSERT**), *Message* — полностью собранное сообщение пользователя отладки, которое должно содержаться в отчете, а **ReturnValue** — это значение, заданное определяемой клиентом функцией отчетов, которая должна возвращаться **_CrtDbgReport**. Полное описание доступных типов отчетов см. в описании функции [_CrtSetReportMode](crtsetreportmode.md).

Если определяемая клиентом функция отчетов полностью обрабатывает сообщение отладки таким, что дальнейшие отчеты не требуются, функция должна возвращать **значение true**. Если функция возвращает **значение false**, вызывается **_CrtDbgReport** для создания отладочного отчета с использованием текущих параметров для типа отчета, режима и файла. Кроме того, указав возвращаемое значение **_CrtDbgReport** в **ReturnValue**, приложение может также контролировать, происходит ли прерывание отладки. Полное описание настройки и создания отчета по отладке см. в разделе **_CrtSetReportMode**, [_CrtSetReportFile](crtsetreportfile.md)и **_CrtDbgReport**.

Дополнительные сведения о других допускающих подключение функциях среды выполнения и написании собственных определяемых клиентом функциях-ловушках см. в разделе [Написание функций отладочных ловушек](/visualstudio/debugger/debug-hook-function-writing).

> [!NOTE]
> Если приложение компилируется с **параметром/CLR** и функция отчетов вызывается после того, как приложение завершило работу, среда CLR выдаст исключение, если функция отчетов вызывает какие-либо функции CRT.

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|**_CrtSetReportHook**|\<crtdbg.h>|

Дополнительные сведения о совместимости см. в разделе [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="libraries"></a>Библиотеки

Только отладочные версии [библиотек времени выполнения языка C](../../c-runtime-library/crt-library-features.md).

## <a name="see-also"></a>См. также раздел

[Отладочные подпрограммы](../../c-runtime-library/debug-routines.md)<br/>
[_CrtGetReportHook](crtgetreporthook.md)<br/>
