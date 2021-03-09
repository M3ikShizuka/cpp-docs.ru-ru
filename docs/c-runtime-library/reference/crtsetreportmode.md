---
title: _CrtSetReportMode
description: 'Дополнительные сведения: _CrtSetReportMode'
ms.date: 3/8/2021
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
ms.openlocfilehash: 770ef955894563dc11dee9f13946067d5d024c11
ms.sourcegitcommit: 90c300b74f6556cb5d989802d2e80d79542f55e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "102514386"
---
# `_CrtSetReportMode`

Задает назначение или назначения для конкретного типа отчета, создаваемого **_CrtDbgReport** , а также любые макросы, которые вызывают [`_CrtDbgReport, _CrtDbgReportW`](crtdbgreport-crtdbgreportw.md) , такие как [ `_ASSERT, _ASSERTE, _ASSERT_EXPR` макросы](assert-asserte-assert-expr-macros.md), [ `_ASSERT, _ASSERTE, _ASSERT_EXPR` макросы](assert-asserte-assert-expr-macros.md), [ `_RPT, _RPTF, _RPTW, _RPTFW` макросы](rpt-rptf-rptw-rptfw-macros.md)и [ `_RPT, _RPTF, _RPTW, _RPTFW` макросы](rpt-rptf-rptw-rptfw-macros.md) (только отладочная версия).

## <a name="syntax"></a>Синтаксис

```C
int _CrtSetReportMode(
   int reportType,
   int reportMode
);
```

### <a name="parameters"></a>Параметры

*`reportType`*\
Тип отчета: **`_CRT_WARN`** , **`_CRT_ERROR`** и **`_CRT_ASSERT`** .

*`reportMode`*\
Новый режим или режимы отчета для *`reportType`* .

## <a name="return-value"></a>Возвращаемое значение

При успешном завершении **`_CrtSetReportMode`** возвращает предыдущий режим или режимы отчета для типа отчета, указанного в *`reportType`* . Если недопустимое значение передается в AS *`reportType`* или для параметра задано недопустимый режим *`reportMode`* , **`_CrtSetReportMode`** вызывает обработчик недопустимых параметров, как описано в разделе [Проверка параметров](../../c-runtime-library/parameter-validation.md). Если выполнение может быть продолжено, эта функция задает **`errno`** для значение **`EINVAL`** и возвращает значение-1. Дополнительные сведения см. в статье [`errno, _doserrno, _sys_errlist, and _sys_nerr`](../../c-runtime-library/errno-doserrno-sys-errlist-and-sys-nerr.md).

## <a name="remarks"></a>Комментарии

**`_CrtSetReportMode`** Указывает назначение выходных данных для **`_CrtDbgReport`** . Поскольку макросы [`_ASSERT`](assert-asserte-assert-expr-macros.md) , [`_ASSERTE`](assert-asserte-assert-expr-macros.md) , [`_RPT`](rpt-rptf-rptw-rptfw-macros.md) и [`_RPTF`](rpt-rptf-rptw-rptfw-macros.md) вызывают **`_CrtDbgReport`** , **`_CrtSetReportMode`** задает выходное назначение для текста, указанного с помощью этих макросов.

Если [`_DEBUG`](../../c-runtime-library/debug.md) не определено, вызовы **`_CrtSetReportMode`** удаляются во время предварительной обработки.

Если не вызвать **`_CrtSetReportMode`** для определения назначения выходных данных сообщений, действуют следующие значения по умолчанию:

- Ошибки и сбои проверочного утверждения направляются в окно сообщений отладчика.

- Предупреждения из Windows-приложений направляются в окно вывода отладчика.

- Предупреждения из консольных приложений не отображаются.

В следующей таблице перечислены типы отчетов, определенные в `Crtdbg.h` .

|Тип отчета|Описание|
|-----------------|-----------------|
|**`_CRT_WARN`**|Предупреждения, сообщения и сведения, не требующие немедленного внимания.|
|**`_CRT_ERROR`**|Ошибки, неустранимые проблемы и ситуации, которые требуют немедленного внимания.|
|**`_CRT_ASSERT`**|Ошибки утверждений (утвержденные выражения, принимающие значение **`FALSE`** ).|

**`_CrtSetReportMode`** Функция присваивает новый режим отчета, указанный в, *`reportMode`* типу отчета, указанному в параметре *`reportType`* , и возвращает ранее определенный режим отчета для *`reportType`* . В следующей таблице перечислены доступные варианты для *`reportMode`* и результирующее поведение **`_CrtDbgReport`** . Эти параметры задаются в виде битовых флагов в файле Crtdbg.h.

|Режим отчета|Поведение функции _CrtDbgReport|
|-----------------|-----------------------------|
|**`_CRTDBG_MODE_DEBUG`**|Выводит сообщение в окно вывода отладчика.|
|**`_CRTDBG_MODE_FILE`**|Выводит сообщение в предоставленный пользователем дескриптор файла. [`_CrtSetReportFile`](crtsetreportfile.md) для определения конкретного файла или потока, используемого в качестве назначения, следует вызвать метод.|
|**`_CRTDBG_MODE_WNDW`**|Создает окно сообщения для вывода сообщения вместе с [`abort`](abort.md) **`Retry`** кнопками, и **Ignore** .|
|**`_CRTDBG_REPORT_MODE`**|Возвращает *`reportMode`* для указанного *`reportType`* :<br /><br /> одного   **`_CRTDBG_MODE_FILE`**<br /><br /> открыт   **`_CRTDBG_MODE_DEBUG`**<br /><br /> четырех   **`_CRTDBG_MODE_WNDW`**|

Каждый тип отчета может создаваться с использованием одного, двух или трех режимов или вообще без режима. Следовательно, для одного типа отчета может быть задано несколько мест назначения. Например, следующий фрагмент кода приводит к тому, что ошибки утверждений отправляются в окно сообщения отладки и в **`stderr`** :

```C
_CrtSetReportMode( _CRT_ASSERT, _CRTDBG_MODE_FILE | _CRTDBG_MODE_WNDW );
_CrtSetReportFile( _CRT_ASSERT, _CRTDBG_FILE_STDERR );
```

Кроме того, режимом или режимами отчетов можно управлять отдельно для каждого типа отчета. Например, можно указать, что объект *`reportType`* **`_CRT_WARN`** должен быть отправлен в выходную отладочную строку, а **`_CRT_ASSERT`** будет отображаться при помощи окна сообщения об отладке и отправить **`stderr`** , как было показано ранее.

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|Необязательный заголовок|
|-------------|---------------------|---------------------|
|**`_CrtSetReportMode`**|`<crtdbg.h>`|`<errno.h>`|

Дополнительные сведения о совместимости см. в разделе [Compatibility](../../c-runtime-library/compatibility.md).

**Библиотеки:** Отладочные версии [библиотек времени выполнения C](../../c-runtime-library/crt-library-features.md) .

## <a name="see-also"></a>См. также

[Отладочные подпрограммы](../../c-runtime-library/debug-routines.md)
