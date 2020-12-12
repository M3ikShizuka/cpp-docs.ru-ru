---
description: 'Дополнительные сведения: _execl, _wexecl'
title: _execl, _wexecl
ms.date: 11/04/2016
api_name:
- _execl
- _wexecl
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
- api-ms-win-crt-process-l1-1-0.dll
api_type:
- DLLExport
topic_type:
- apiref
f1_keywords:
- _execl
- _wexecl
- wexecl
helpviewer_keywords:
- _execl function
- wexecl function
- _wexecl function
- execl function
ms.assetid: 81fefb8a-0a06-4221-b2bc-be18e38e89f4
ms.openlocfilehash: 8775dbae1f566ff42aeadaedf310323cfca410ee
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97305004"
---
# <a name="_execl-_wexecl"></a>_execl, _wexecl

Загружает и выполняет новые дочерние процессы.

> [!IMPORTANT]
> Этот API нельзя использовать в приложениях, выполняемых в среде выполнения Windows. Дополнительные сведения: [Функции CRT, которые не поддерживаются в приложениях универсальной платформы Windows](../../cppcx/crt-functions-not-supported-in-universal-windows-platform-apps.md).

## <a name="syntax"></a>Синтаксис

```C
intptr_t _execl(
   const char *cmdname,
   const char *arg0,
   ... const char *argn,
   NULL
);
intptr_t _wexecl(
   const wchar_t *cmdname,
   const wchar_t *arg0,
   ... const wchar_t *argn,
   NULL
);
```

### <a name="parameters"></a>Параметры

*кмднаме*<br/>
Путь к выполняемому файлу.

*arg0*,... *argN*<br/>
Список указателей на параметры.

## <a name="return-value"></a>Возвращаемое значение

В случае успешного выполнения эти функции не возвращаются к вызывающему процессу. Возвращаемое значение, равное-1, **указывает на ошибку** . в этом случае задается глобальная переменная «пробуждение».

|Значение errno|Описание|
|-----------------|-----------------|
|**E2BIG**|Пространство, требуемое для аргументов и параметров среды, превышает 32 КБ.|
|**еакцес**|Указанный файл имеет нарушение блокировки или общего доступа.|
|**еинвал**|Недопустимый параметр (один или несколько параметров представляли собой указатель null или пустую строку).|
|**EMFILE**|Открыто слишком много файлов (указанный файл необходимо открыть и определить, является ли он исполняемым).|
|**еноент**|Файл или путь не найден.|
|**ENOEXEC**|Указанный файл не является исполняемым или имеет недопустимый формат исполняемого файла.|
|**еномем**|Недостаточно доступной памяти для выполнения нового процесса; либо доступная память повреждена, либо существует недопустимый блок, что указывает на неправильное выделение памяти для процесса, а значит вызывающий процесс был выделен ненадлежащим образом.|

## <a name="remarks"></a>Комментарии

Каждая из этих функций загружает и выполняет новый процесс, передавая все аргументы командной строки как отдельные параметры. Первым аргументом является имя команды или исполняемого файла, а второй должен быть таким же, как первый. В процессе запуска он становится `argv[0]`. Третий аргумент — это первый аргумент, `argv[1]`, выполняемого процесса.

Функции **_execl** проверяют свои параметры. Если *кмднаме* или *arg0* является пустым указателем или пустой строкой, эти функции вызывают обработчик недопустимых параметров, как описано в разделе [Проверка параметров](../../c-runtime-library/parameter-validation.md) , если выполнение может быть продолжено, эти **функции устанавливают в значение** **еинвал** и возвращают-1. Новые процессы не выполняются.

## <a name="requirements"></a>Требования

|Функция|Обязательный заголовок|Необязательный заголовок|
|--------------|---------------------|---------------------|
|**_execl**|\<process.h>|\<errno.h>|
|**_wexecl**|\<process.h> или \<wchar.h>|\<errno.h>|

Дополнительные сведения о совместимости см. в разделе [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="example"></a>Пример

См. пример в разделе [Функции _exec, _wexec](../../c-runtime-library/exec-wexec-functions.md).

## <a name="see-also"></a>См. также раздел

[Управление процессами и средой](../../c-runtime-library/process-and-environment-control.md)<br/>
[_exec, функции _wexec](../../c-runtime-library/exec-wexec-functions.md)<br/>
[рвал](abort.md)<br/>
[atexit](atexit.md)<br/>
[exit, _Exit, _exit](exit-exit-exit.md)<br/>
[_onexit, _onexit_m](onexit-onexit-m.md)<br/>
[_spawn, функции _wspawn](../../c-runtime-library/spawn-wspawn-functions.md)<br/>
[system, _wsystem](system-wsystem.md)<br/>
