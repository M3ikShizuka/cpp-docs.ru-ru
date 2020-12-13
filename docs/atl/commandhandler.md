---
description: 'Дополнительные сведения о: Коммандхандлер'
title: CommandHandler
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- CommandHandler function
ms.assetid: 662bc7bf-4a10-42b3-986d-d8bae4f63551
ms.openlocfilehash: 746048dd83088cac8316cf6e0140644956c21b4b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97153288"
---
# <a name="commandhandler"></a>CommandHandler

`CommandHandler` функция, определяемая третьим параметром макроса COMMAND_HANDLER в схеме сообщений.

## <a name="syntax"></a>Синтаксис

```cpp
LRESULT CommandHandler(
    WORD wNotifyCode,
    WORD wID,
    HWND hWndCtl,
    BOOL& bHandled);
```

#### <a name="parameters"></a>Параметры

*wNotifyCode*<br/>
Код уведомления.

*wID*<br/>
Идентификатор элемента меню, элемента управления или ускорителя.

*хвндктл*<br/>
Маркер для элемента управления "окно".

*бхандлед*<br/>
Схема сообщений устанавливает для *бхандлед* значение true перед `CommandHandler` вызовом метода. Если `CommandHandler` не полностью обрабатывает сообщение, необходимо установить *бхандлед* в значение false, чтобы указать, что сообщение требует дальнейшей обработки.

## <a name="return-value"></a>Возвращаемое значение

Результат обработки сообщения. 0 в случае успеха.

## <a name="remarks"></a>Комментарии

Пример использования этого обработчика сообщений в схеме сообщений см. в разделе [COMMAND_HANDLER](reference/message-map-macros-atl.md#command_handler).

## <a name="see-also"></a>См. также раздел

[Реализация окна](../atl/implementing-a-window.md)<br/>
[Схемы сообщений](../atl/message-maps-atl.md)<br/>
[WM_NOTIFY](/windows/win32/controls/wm-notify)
