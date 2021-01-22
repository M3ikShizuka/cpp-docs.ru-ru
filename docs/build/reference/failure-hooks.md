---
description: 'Дополнительные сведения: перехватчики сбоев отложенной загрузки'
title: Обработчики сбоев
ms.date: 01/19/2021
helpviewer_keywords:
- delayed loading of DLLs, failure hooks
ms.openlocfilehash: 46cec6c66169ebe589bb5f0c912b2d8239e69da1
ms.sourcegitcommit: 3d9cfde85df33002e3b3d7f3509ff6a8dc4c0a21
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/21/2021
ms.locfileid: "98667175"
---
# <a name="failure-hooks"></a>Обработчики сбоев

Ловушка сбоя включена так же, как [обработчик уведомлений](notification-hooks.md). Подпрограммы-ловушки должны возвращать подходящее значение, чтобы обработка могла продолжаться ( `HINSTANCE` или `FARPROC` ), или 0, чтобы указать, что должно быть создано исключение.

Переменная указателя, ссылающаяся на определяемую пользователем функцию, имеет следующие вид:

```C
// This is the failure hook, dliNotify = {dliFailLoadLib|dliFailGetProc}
ExternC
PfnDliHook   __pfnDliFailureHook2;
```

**`DelayLoadInfo`** Структура содержит все соответствующие данные, необходимые для точной отчетности об ошибке, включая значение из `GetLastError` .

Если уведомление имеет значение **`dliFailLoadLib`** , функция-обработчик может вернуть:

- 0, если не удается справиться с ошибкой.

- Значение `HMODULE` , если обработчик сбоев устранил проблему и загрузил саму библиотеку.

Если уведомление имеет значение **`dliFailGetProc`** , функция-обработчик может вернуть:

- 0, если не удается справиться с ошибкой.

- Допустимый адрес процедуры (адрес функции импорта), если обработчик сбоев успешно получает адрес.

## <a name="see-also"></a>См. также раздел

[Обработка ошибок и предупреждений](error-handling-and-notification.md)
