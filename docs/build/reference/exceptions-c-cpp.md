---
description: 'Дополнительные сведения: исключения с задержкой загрузки (C/C++)'
title: Коды исключений при задержке загрузки DLL
ms.date: 01/19/2021
f1_keywords:
- ERROR_MOD_NOT_FOUND
- vcppException
- ERROR_SEVERITY_ERROR
helpviewer_keywords:
- vcppException
- C++ exception handling, delayed loading of DLLs
- delayed loading of DLLs, exceptions
- ERROR_SEVERITY_ERROR exception
- ERROR_MOD_NOT_FOUND exception
ms.openlocfilehash: 214d8514baba7b180b8d838af8a6b6c0543cc1ce
ms.sourcegitcommit: 3d9cfde85df33002e3b3d7f3509ff6a8dc4c0a21
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/21/2021
ms.locfileid: "98667192"
---
# <a name="dll-delay-load-exception-codes"></a>Коды исключений при задержке загрузки DLL

При возникновении ошибок могут возникать два структурированных кода исключений:

- Для `LoadLibrary` сбоя

- Для `GetProcAddress` сбоя

Ниже приведен макрос сведений об исключении:

```C
//
// Exception information
//
#define FACILITY_VISUALCPP  ((LONG)0x6d)
#define VcppException(sev,err)  ((sev) | (FACILITY_VISUALCPP<<16) | err)
```

Вызываемые коды исключений — это `VcppException(ERROR_SEVERITY_ERROR, ERROR_MOD_NOT_FOUND)` стандартные `VcppException(ERROR_SEVERITY_ERROR, ERROR_PROC_NOT_FOUND)` значения и. Исключение передает указатель на `DelayLoadInfo` структуру в `LPDWORD` значении, которое может быть извлечено `GetExceptionInformation` в [`EXCEPTION_RECORD`](/windows/win32/api/winnt/ns-winnt-exception_record) структуре в `ExceptionInformation[0]` поле.

Кроме того, если в поле заданы неправильные биты `grAttrs` , возникает исключение `ERROR_INVALID_PARAMETER` . Это исключение для всех целей и назначений, неустранимое.

Дополнительные сведения см. в разделе [определения структуры и константы](structure-and-constant-definitions.md).

## <a name="see-also"></a>См. также раздел

[Обработка ошибок и предупреждений](error-handling-and-notification.md)
