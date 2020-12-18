---
description: 'Подробнее о следующем: Имена сред'
title: Имена сред
ms.date: 11/04/2016
ms.assetid: 9af409a5-e724-465a-9a21-88d3586c2e92
ms.openlocfilehash: f40da15151385cea4bd581dea8946f50d2b58ea8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97213758"
---
# <a name="environment-names"></a>Имена сред

**ANSI 4.10.4.4** Набор имен среды и метод, который используется для изменения списка среды, используемого функцией [getenv](../c-runtime-library/reference/getenv-wgetenv.md)

Набор имен среды не ограничен.

Чтобы изменить переменные среды из программы на языке C, вызовите функцию [_putenv](../c-runtime-library/reference/putenv-wputenv.md). Чтобы изменить переменные среды из командной строки в Windows, используйте команду SET (например, SET LIB = D:\ LIBS).

Переменные среды, заданные в программе на языке C, существуют, только пока выполняется копия узла командной оболочки операционной системы (CMD.EXE или COMMAND.COM). Например, в строке

```
system( SET LIB = D:\LIBS );
```

выполняется копия командной оболочки (CMD.EXE), задается переменная среды LIB и выполняется возврат в программу на языке C при выходе из дополнительной копии CMD.EXE. При выходе из этой копии CMD.EXE временная переменная среды LIB удаляется.

Таким же образом, изменения, выполненные функцией `_putenv`, действуют только до завершения программы.

## <a name="see-also"></a>См. также

[Функции библиотеки](../c-language/library-functions.md)<br/>
[_putenv, _wputenv](../c-runtime-library/reference/putenv-wputenv.md)<br/>
[getenv, _wgetenv](../c-runtime-library/reference/getenv-wgetenv.md)
