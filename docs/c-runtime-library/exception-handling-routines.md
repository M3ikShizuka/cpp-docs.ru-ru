---
description: 'Дополнительные сведения: подпрограммы обработки исключений'
title: Процедуры обработки исключений
ms.date: 11/04/2016
f1_keywords:
- c.exceptions
helpviewer_keywords:
- exception handling, routines
ms.assetid: f60548c6-850a-4e1e-a79b-a2a6a541ab62
ms.openlocfilehash: d241c3ef7f32a96f08d4ad499887963fda031967
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97331099"
---
# <a name="exception-handling-routines"></a>Процедуры обработки исключений

Использование функций обработки исключений C++ для восстановления после непредвиденных событий во время выполнения программы.

## <a name="exception-handling-functions"></a>Функции обработки исключений

|Функция|Использовать|
|--------------|---------|
|[_set_se_translator](../c-runtime-library/reference/set-se-translator.md)|Обрабатывает исключения Win32 (структурированные исключения C) как типизированные исключения C++|
|[set_terminate](../c-runtime-library/reference/set-terminate-crt.md)|Установите собственную подпрограмму завершения, чтобы ее можно было вызвать с помощью функции **terminate**|
|[set_unexpected](../c-runtime-library/reference/set-unexpected-crt.md)|Установите собственную функцию завершения, которая будет вызываться **unexpected**.|
|[заканчива](../c-runtime-library/reference/terminate-crt.md)|Вызывается автоматически при определенных условиях после исключения. Функция **terminate** вызывает функцию **abort** или функцию, указанную с помощью **set_terminate**.|
|[известно](../c-runtime-library/reference/unexpected-crt.md)|Вызывает **terminate** или функцию, указанную с помощью **set_unexpected**. Функция **unexpected** не используется в текущей реализации обработчика исключений Microsoft C++.|

## <a name="see-also"></a>См. также раздел

[Подпрограммы универсальной среды выполнения C по категориям](../c-runtime-library/run-time-routines-by-category.md)<br/>
