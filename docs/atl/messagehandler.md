---
description: 'Дополнительные сведения о: Мессажехандлер'
title: MessageHandler
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- MessageHandler function
ms.assetid: 8a0acf97-1b0d-4226-91b9-75446634a03c
ms.openlocfilehash: d369b94721e57eb4adc704570bc09d1aae184fe1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97159509"
---
# <a name="messagehandler"></a>MessageHandler

`MessageHandler` имя функции, определяемой вторым параметром макроса MESSAGE_HANDLER в схеме сообщений.

## <a name="syntax"></a>Синтаксис

```cpp
LRESULT MessageHandler(
    UINT uMsg,
    WPARAM wParam,
    LPARAM lParam,
    BOOL& bHandled);
```

### <a name="parameters"></a>Параметры

*Uiacp*<br/>
Задает сообщение.

*wParam*<br/>
Дополнительные сведения, относящиеся к сообщению.

*lParam*<br/>
Дополнительные сведения, относящиеся к сообщению.

*бхандлед*<br/>
Схема сообщений устанавливает для *бхандлед* значение true перед `MessageHandler` вызовом метода. Если `MessageHandler` не полностью обрабатывает сообщение, необходимо установить *бхандлед* в значение false, чтобы указать, что сообщение требует дальнейшей обработки.

## <a name="return-value"></a>Возвращаемое значение

Результат обработки сообщения. 0 в случае успеха.

## <a name="remarks"></a>Комментарии

Пример использования этого обработчика сообщений в схеме сообщений см. в разделе [MESSAGE_HANDLER](reference/message-map-macros-atl.md#message_handler).

## <a name="see-also"></a>См. также раздел

[Реализация окна](../atl/implementing-a-window.md)<br/>
[Схемы сообщений](../atl/message-maps-atl.md)<br/>
[WM_NOTIFY](/windows/win32/controls/wm-notify)
