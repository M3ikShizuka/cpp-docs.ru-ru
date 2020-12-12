---
description: 'Дополнительные сведения: создание обработчика завершения'
title: Написание обработчика завершения
ms.date: 11/04/2016
helpviewer_keywords:
- structured exception handling [C++], termination handlers
- exceptions [C++], terminating
- termination handlers [C++], writing
- handlers [C++]
- handlers [C++], termination
- termination handlers
- exception handling [C++], termination handlers
- try-catch keyword [C++], termination handlers
ms.assetid: 52aa1f8f-f8dd-44b8-be94-5e2fc88d44fb
ms.openlocfilehash: a203cab7d61be66c5fe919aefe1895aa0928c5d9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97302989"
---
# <a name="writing-a-termination-handler"></a>Написание обработчика завершения

В отличие от обработчика исключений, обработчик завершения выполняется всегда независимо от того, завершен ли в обычном режиме защищенный блок кода. Единственным назначением обработчика завершения должна быть проверка правильности закрытия таких ресурсов, как память, дескрипторы и файлы, независимо от того, как завершается выполнение фрагмента кода.

Обработчики завершения используют оператор try-finally.

## <a name="what-do-you-want-to-know-more-about"></a>Дополнительные сведения

- [Оператор try-finally](../cpp/try-finally-statement.md)

- [Освобождение ресурсов](../cpp/cleaning-up-resources.md)

- [Время действий в обработке исключений](../cpp/timing-of-exception-handling-a-summary.md)

- [Ограничения обработчиков завершения](../cpp/restrictions-on-termination-handlers.md)

## <a name="see-also"></a>См. также раздел

[Structured Exception Handling (C/C++)](../cpp/structured-exception-handling-c-cpp.md)
