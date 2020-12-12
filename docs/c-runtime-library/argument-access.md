---
description: 'Дополнительные сведения: доступ к аргументам'
title: Доступ к аргументам
ms.date: 04/04/2018
f1_keywords:
- c.arguments
helpviewer_keywords:
- argument access macros [C++]
- variable-length argument lists
ms.assetid: 7046ae34-a0ec-44f0-815d-3209492a3e19
ms.openlocfilehash: f62ac2bc4ae895afe763d0a0a4caa32601e82713
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97221869"
---
# <a name="argument-access"></a>Доступ к аргументам

Макросы **va_arg**, **va_end** и **va_start** предоставляют доступ к аргументам функций, когда число аргументов является переменным. Эти макросы определены в \<stdarg.h> для совместимости с ANSI/ISO C и \<varargs.h> для СОВМЕСТИМОСТИ с UNIX System V.

## <a name="argument-access-macros"></a>Макросы для доступа к аргументам

|Макрос|Использовать|
|-----------|-------------------------------|
|[va_arg](../c-runtime-library/reference/va-arg-va-copy-va-end-va-start.md)|Извлечение аргумента из списка|
|[va_end](../c-runtime-library/reference/va-arg-va-copy-va-end-va-start.md)|Сброс указателя|
|[va_start](../c-runtime-library/reference/va-arg-va-copy-va-end-va-start.md)|Установка указателя на начало списка аргументов|

## <a name="see-also"></a>См. также раздел

[Подпрограммы универсальной среды выполнения C по категориям](../c-runtime-library/run-time-routines-by-category.md)
