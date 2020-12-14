---
description: 'Дополнительные сведения: _pclose'
title: _pclose
ms.date: 4/2/2020
api_name:
- _pclose
- _o__pclose
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
- api-ms-win-crt-stdio-l1-1-0.dll
- api-ms-win-crt-private-l1-1-0.dll
api_type:
- DLLExport
topic_type:
- apiref
f1_keywords:
- _pclose
- pclose
helpviewer_keywords:
- _pclose function
- pclose function
- pipes, closing
ms.assetid: e2e31a9e-ba3a-4124-bcbb-c4040110b3d3
ms.openlocfilehash: 529af8ccdd1c6cc27f9039adef5d75c8b977aa54
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97258711"
---
# <a name="_pclose"></a>_pclose

Ожидает новый обработчик команд и закрывает поток по связанному каналу.

> [!IMPORTANT]
> Этот API нельзя использовать в приложениях, выполняемых в среде выполнения Windows. Дополнительные сведения: [Функции CRT, которые не поддерживаются в приложениях универсальной платформы Windows](../../cppcx/crt-functions-not-supported-in-universal-windows-platform-apps.md).

## <a name="syntax"></a>Синтаксис

```C
int _pclose(
FILE *stream
);
```

### <a name="parameters"></a>Параметры

*вышестоящий*<br/>
Возвращаемое значение из предыдущего вызова метода **_popen**.

## <a name="return-value"></a>Возвращаемое значение

Возвращает состояние выхода для завершающего обработчика команд или-1 при возникновении ошибки. Формат возвращаемого значения тот же, что и для **_cwait**, за исключением того, что байты нижнего и верхнего порядка меняются местами. Если Stream имеет **значение NULL**, **_Pclose** **устанавливает** **нееинвал** и возвращает-1.

Дополнительные сведения об этих и других кодах ошибок см. в разделе [_doserrno, errno, _sys_errlist и _sys_nerr](../../c-runtime-library/errno-doserrno-sys-errlist-and-sys-nerr.md).

## <a name="remarks"></a>Комментарии

Функция **_pclose** ищет идентификатор процесса обработчика команд (Cmd.exe), запущенный связанным вызовом **_popen** , выполняет [_cwait](cwait.md) вызов в новом обработчике команд и закрывает поток в соответствующем канале.

По умолчанию глобальное состояние этой функции ограничивается приложением. Чтобы изменить это, см. раздел [глобальное состояние в CRT](../global-state.md).

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|**_pclose**|\<stdio.h>|

Дополнительные сведения о совместимости см. в разделе [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="libraries"></a>Библиотеки

Все версии [библиотек времени выполнения языка C](../../c-runtime-library/crt-library-features.md).

## <a name="see-also"></a>См. также раздел

[Управление процессами и средой](../../c-runtime-library/process-and-environment-control.md)<br/>
[_pipe](pipe.md)<br/>
[_popen, _wpopen](popen-wpopen.md)<br/>
