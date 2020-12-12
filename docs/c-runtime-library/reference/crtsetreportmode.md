---
description: 'Дополнительные сведения: _CrtSetReportMode'
title: _CrtSetReportMode
ms.date: 11/04/2016
api_name:
- _CrtSetReportMode
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
- _CrtSetReportMode
- CrtSetReportMode
helpviewer_keywords:
- _CrtSetReportMode function
- CrtSetReportMode function
ms.assetid: 3ecc6a12-afdd-4242-b046-8187ff6d4b36
ms.openlocfilehash: 645a9f8ddf1a1725319eba7a83d9f63270bbed8a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97279823"
---
# <a name="_crtsetreportmode"></a>_CrtSetReportMode

Задает назначение или назначения для конкретного типа отчета, создаваемого **_CrtDbgReport** , а также любые макросы, вызывающие [_CrtDbgReport, _CrtDbgReportW](crtdbgreport-crtdbgreportw.md), такие как [_ASSERT, _ASSERTE, _ASSERT_EXPR макросы](assert-asserte-assert-expr-macros.md), [_ASSERT, _ASSERTE, _ASSERT_EXPR макросы](assert-asserte-assert-expr-macros.md), _RPT, _RPTF, _RPTW, [макросы](rpt-rptf-rptw-rptfw-macros.md)и [_RPTFW, _RPT, _RPTF, _RPTW макросы](rpt-rptf-rptw-rptfw-macros.md) (только отладочная версия).

## <a name="syntax"></a>Синтаксис

```C
int _CrtSetReportMode(
   int reportType,
   int reportMode
);
```

### <a name="parameters"></a>Параметры

*reportType*<br/>
Тип отчета: **_CRT_WARN**, **_CRT_ERROR** и **_CRT_ASSERT**.

*репортмоде*<br/>
Новый режим или режимы работы с отчетами для *reportType*.

## <a name="return-value"></a>Возвращаемое значение

При успешном завершении **_CrtSetReportMode** возвращает предыдущий режим или режимы отчета для типа отчета, указанного в *reportType*. Если в качестве *reportType* передается недопустимое значение или для *репортмоде* указан недопустимый режим, **_CrtSetReportMode** вызывает обработчик недопустимых параметров, как описано в разделе [Проверка параметров](../../c-runtime-library/parameter-validation.md). Если выполнение может быть продолжено, эта функция **устанавливает** **еинвал** и возвращает-1. Дополнительные сведения см. в разделе [errno, _doserrno, _sys_errlist и _sys_nerr](../../c-runtime-library/errno-doserrno-sys-errlist-and-sys-nerr.md).

## <a name="remarks"></a>Комментарии

**_CrtSetReportMode** указывает назначение выходных данных для **_CrtDbgReport**. Поскольку макросы [_ASSERT](assert-asserte-assert-expr-macros.md), [_ASSERTE](assert-asserte-assert-expr-macros.md), [_RPT](rpt-rptf-rptw-rptfw-macros.md)и [_RPTF](rpt-rptf-rptw-rptfw-macros.md) вызывают **_CrtDbgReport**, **_CrtSetReportMode** указывает назначение вывода текста, указанного с помощью этих макросов.

Если [_DEBUG](../../c-runtime-library/debug.md) не определено, вызовы **_CrtSetReportMode** удаляются во время предварительной обработки.

Если не вызвать **_CrtSetReportMode** для определения назначения вывода сообщений, действуют следующие значения по умолчанию:

- Ошибки и сбои проверочного утверждения направляются в окно сообщений отладчика.

- Предупреждения из Windows-приложений направляются в окно вывода отладчика.

- Предупреждения из консольных приложений не отображаются.

В следующей таблице перечислены типы сообщений, определенные в файле Crtdbg.h.

|Тип отчета|Описание|
|-----------------|-----------------|
|**_CRT_WARN**|Предупреждения, сообщения и сведения, не требующие немедленного внимания.|
|**_CRT_ERROR**|Ошибки, неустранимые проблемы и ситуации, которые требуют немедленного внимания.|
|**_CRT_ASSERT**|Ошибки утверждений (утвержденные выражения, принимающие **значение false**).|

Функция **_CrtSetReportMode** назначает новый режим отчета, указанный в *репортмоде* , типу отчета, указанному в *reportType* , и возвращает ранее определенный режим отчета для *reportType*. В следующей таблице перечислены доступные варианты для *репортмоде* и результирующее поведение **_CrtDbgReport**. Эти параметры задаются в виде битовых флагов в файле Crtdbg.h.

|Режим отчета|Поведение функции _CrtDbgReport|
|-----------------|-----------------------------|
|**_CRTDBG_MODE_DEBUG**|Выводит сообщение в окно вывода отладчика.|
|**_CRTDBG_MODE_FILE**|Выводит сообщение в предоставленный пользователем дескриптор файла. Для определения конкретного файла или потока, используемого в качестве места назначения, необходимо вызвать функцию [_CrtSetReportFile](crtsetreportfile.md).|
|**_CRTDBG_MODE_WNDW**|Создает окно сообщения для вывода сообщения вместе с кнопками [прервать](abort.md), **повторить** и **пропустить** .|
|**_CRTDBG_REPORT_MODE**|Возвращает *репортмоде* для указанного *reportType*:<br /><br /> 1   **_CRTDBG_MODE_FILE**<br /><br /> 2   **_CRTDBG_MODE_DEBUG**<br /><br /> 4   **_CRTDBG_MODE_WNDW**|

Каждый тип отчета может создаваться с использованием одного, двух или трех режимов или вообще без режима. Следовательно, для одного типа отчета может быть задано несколько мест назначения. Например, следующий фрагмент кода вызывает отправку проверочных ошибок как в окно сообщения отладки, так и в **stderr**:

```C
_CrtSetReportMode( _CRT_ASSERT, _CRTDBG_MODE_FILE | _CRTDBG_MODE_WNDW );
_CrtSetReportFile( _CRT_ASSERT, _CRTDBG_FILE_STDERR );
```

Кроме того, режимом или режимами отчетов можно управлять отдельно для каждого типа отчета. Например, можно указать, что *reportType* **_CRT_WARN** быть отправлены в выходную строку отладки, а **_CRT_ASSERT** отображаться с помощью окна сообщения об отладке и отправлять в **stderr**, как было показано ранее.

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|Необязательный заголовок|
|-------------|---------------------|---------------------|
|**_CrtSetReportMode**|\<crtdbg.h>|\<errno.h>|

Дополнительные сведения о совместимости см. в разделе [Compatibility](../../c-runtime-library/compatibility.md).

**Библиотеки:** только отладочные версии [функций библиотеки CRT](../../c-runtime-library/crt-library-features.md).

## <a name="see-also"></a>См. также раздел

[Отладочные подпрограммы](../../c-runtime-library/debug-routines.md)<br/>
