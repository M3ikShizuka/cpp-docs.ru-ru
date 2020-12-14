---
description: 'Дополнительные сведения: создание обработчика исключений'
title: Написание обработчика исключений
ms.date: 11/04/2016
helpviewer_keywords:
- structured exception handling [C++], exception handlers
- exception handling [C++], exception handlers
ms.assetid: 71473fee-f773-4a34-bf12-82a3af79579c
ms.openlocfilehash: 174ab77240fc405e7c1175806167b6ec68f08c82
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97302807"
---
# <a name="writing-an-exception-handler"></a>Написание обработчика исключений

Обработчики исключений обычно используются для ответа на конкретные ошибки. Можно использовать синтаксис обработки исключений, чтобы фильтровать все исключения, отличные от тех, которые вы знаете, как обработать. Прочие исключения должны передаваться другим обработчикам (возможно, в библиотеке среды выполнения или ОС), созданным для поиска этих конкретных исключений.

Обработчики исключений используют оператор try-except.

## <a name="what-do-you-want-to-know-more-about"></a>Дополнительные сведения

- [Оператор try-except](../cpp/try-except-statement.md)

- [Написание фильтра исключений](../cpp/writing-an-exception-filter.md)

- [Создание исключений программного обеспечения](../cpp/raising-software-exceptions.md)

- [Исключения оборудования](../cpp/hardware-exceptions.md)

- [Ограничения обработчиков исключений](../cpp/restrictions-on-exception-handlers.md)

## <a name="see-also"></a>См. также раздел

[Structured Exception Handling (C/C++)](../cpp/structured-exception-handling-c-cpp.md)
