---
description: 'Дополнительные сведения: _except_handler3'
title: _except_handler3
ms.date: 1/14/2021
api_name:
- _except_handler3
api_location:
- msvcrt.dll
- msvcr90.dll
- msvcr80.dll
- msvcr110_clr0400.dll
- msvcr120.dll
- msvcr100.dll
- msvcr110.dll
- api-ms-win-crt-private-l1-1-0.dll
api_type:
- DLLExport
topic_type:
- apiref
f1_keywords:
- _except_handler3
- except_handler3
helpviewer_keywords:
- _except_handler3 function
- except_handler3 function
ms.assetid: b0c64898-0ae5-48b7-9724-80135a0813e2
ms.openlocfilehash: fdeefce15401530468976cba1be737ac13512ccb
ms.sourcegitcommit: 1cd8f8a75fd036ffa57bc70f3ca869042d8019d4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "98242999"
---
# <a name="_except_handler3"></a>_except_handler3

Внутренняя функция CRT. Используется платформой для поиска подходящего обработчика исключений для обработки текущего исключения.

## <a name="syntax"></a>Синтаксис

```
int _except_handler3(
   PEXCEPTION_RECORD exception_record,
   PEXCEPTION_REGISTRATION registration,
   PCONTEXT context,
   PEXCEPTION_REGISTRATION dispatcher
);
```

#### <a name="parameters"></a>Параметры

*exception_record*<br/>
[in] Сведения о конкретном исключении.

*зарегистрировать*<br/>
[in] Запись, которая указывает, какую таблицу области видимости следует использовать для поиска обработчика исключений.

*context*<br/>
[in] Зарезервировано.

*Dispatcher*<br/>
[in] Зарезервировано.

## <a name="return-value"></a>Возвращаемое значение

Если исключение должно быть отброшено, возвращает значение `DISPOSITION_DISMISS`. Если исключение должно быть передано на уровень вверх в инкапсулируемые обработчики исключений, возвращает значение `DISPOSITION_CONTINUE_SEARCH`.

## <a name="remarks"></a>Комментарии

Если этот метод находит подходящий обработчик исключений, он передает исключение в обработчик. В этой ситуации метод не возвращается к вызвавшему его коду, и возвращаемое значение несущественно.

## <a name="see-also"></a>См. также

[Алфавитный справочник по функциям](../c-runtime-library/reference/crt-alphabetical-function-reference.md)
