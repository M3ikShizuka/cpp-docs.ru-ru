---
description: 'Дополнительные сведения: quick_exit'
title: quick_exit1
ms.date: 11/04/2016
api_name:
- quick_exit
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
- api-ms-win-crt-runtime-l1-1-0.dll
api_type:
- DLLExport
topic_type:
- apiref
f1_keywords:
- quick_exit
- process/quick_exit
- stdlib/quick_exit
helpviewer_keywords:
- quick_exit function
ms.assetid: ecfbdae6-01c4-45fa-aaeb-b368e1de2a9c
ms.openlocfilehash: 85640af902092d5cc60a1c718dfd8999c41406b3
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97137102"
---
# <a name="quick_exit"></a>quick_exit

Приводит к завершению работы программы в обычном режиме.

## <a name="syntax"></a>Синтаксис

```C
__declspec(noreturn) void quick_exit(
    int status
);
```

### <a name="parameters"></a>Параметры

*status*<br/>
Код состояния, возвращаемый средой размещения.

## <a name="return-value"></a>Возвращаемое значение

Функция **quick_exit** не может вернуться к ее вызывающему объекту.

## <a name="remarks"></a>Комментарии

Функция **quick_exit** вызывает нормальное завершение программы. Он не вызывает функции, зарегистрированные **atexit**, **_onexit** или обработчики сигналов, зарегистрированные функцией **Signal** . Поведение не определено, если **quick_exit** вызывается более одного раза или если также вызывается функция **Exit** .

Функция **quick_exit** вызывает метод, в порядке "последним подела, первым обслужен" (ЛИФО), функции, зарегистрированные **at_quick_exit**, за исключением тех функций, которые уже были вызваны при регистрации функции.  Поведение не определено, если вызов [longjmp](longjmp.md) осуществляется во время вызова зарегистрированной функции, который привел бы к прерыванию вызова функции.

После вызова зарегистрированных функций **quick_exit** вызывает **_Exit** , используя значение *Status* , чтобы вернуть управление среде узла.

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|**quick_exit**|\<process.h> или \<stdlib.h>|

Дополнительные сведения о совместимости см. в разделе [Совместимость](../../c-runtime-library/compatibility.md).

## <a name="see-also"></a>См. также раздел

[Управление процессами и средой](../../c-runtime-library/process-and-environment-control.md)<br/>
[рвал](abort.md)<br/>
[atexit](atexit.md)<br/>
[_exec, функции _wexec](../../c-runtime-library/exec-wexec-functions.md)<br/>
[exit, _Exit, _exit](exit-exit-exit.md)<br/>
[_onexit, _onexit_m](onexit-onexit-m.md)<br/>
[_spawn, функции _wspawn](../../c-runtime-library/spawn-wspawn-functions.md)<br/>
[system, _wsystem](system-wsystem.md)<br/>
