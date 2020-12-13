---
description: 'Дополнительные сведения: обработка ошибок (CRT)'
title: Обработка ошибок (CRT)
ms.date: 11/04/2016
helpviewer_keywords:
- error handling, C routines for
- logic errors
- error handling, library routines
- testing, for program errors
ms.assetid: 125ac697-9eb0-4152-a440-b7842f23d97f
ms.openlocfilehash: 4aa81f1152fe991398b38f6b433993aecb8be401
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97331141"
---
# <a name="error-handling-crt"></a>Обработка ошибок (CRT)

Используйте эти подпрограммы для обработки ошибок в программах.

## <a name="error-handling-routines"></a>Процедуры обработки ошибок

|Подпрограмма|Использовать|
|-------------|---------|
|Макрос [assert](../c-runtime-library/reference/assert-macro-assert-wassert.md)|Проверка на наличие ошибок в логике программы; доступен как в итоговой, так и в отладочной версии библиотек среды выполнения.|
|Макросы [_ASSERT, _ASSERTE](../c-runtime-library/reference/assert-asserte-assert-expr-macros.md)|Подобны **assert**, но доступны только в отладочных версиях библиотеки времени выполнения.|
|[clearerr](../c-runtime-library/reference/clearerr.md)|Сброс индикатора ошибки. Вызов **rewind** или закрытие потока также приводит к сбросу индикатора ошибки.|
|[_eof](../c-runtime-library/reference/eof.md)|Поиск конца файла в низкоуровневых операциях ввода-вывода.|
|[feof](../c-runtime-library/reference/feof.md)|Проверка на наличие конца файла. Конец файла также указан, если **_read** возвращает результат 0.|
|[ferror](../c-runtime-library/reference/ferror.md)|Проверка на наличие ошибок потокового ввода-вывода.|
|Макросы [_RPT, _RPTF](../c-runtime-library/reference/rpt-rptf-rptw-rptfw-macros.md)|Создают отчет, подобный **printf**, но доступны только в отладочных версиях библиотеки среды выполнения.|
|[_set_error_mode](../c-runtime-library/reference/set-error-mode.md)|Изменяет **__error_mode** для определения отличного от используемого по умолчанию расположения, куда среда выполнения C записывает сообщение об ошибке для ошибок, которые могут вызвать завершение программы.|
|[_set_purecall_handler](../c-runtime-library/reference/get-purecall-handler-set-purecall-handler.md)|Задает обработчик для вызова чистой виртуальной функции.|

## <a name="see-also"></a>См. также раздел

- [Подпрограммы универсальной среды выполнения C по категориям](../c-runtime-library/run-time-routines-by-category.md)
