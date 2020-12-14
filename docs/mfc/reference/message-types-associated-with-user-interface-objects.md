---
description: 'Дополнительные сведения: типы сообщений, связанные с объектами User-Interface'
title: Типы сообщений, связанных с объектами пользовательского интерфейса
ms.date: 11/04/2016
f1_keywords:
- vc.codewiz.uiobject.msgs
helpviewer_keywords:
- message types and user interface objects [MFC]
ms.assetid: 681ee1a7-f6e6-4ea0-9fc6-1fb53a35516e
ms.openlocfilehash: 78ddb9e5290d17f92714d6b50a57ac097bbf104c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97219282"
---
# <a name="message-types-associated-with-user-interface-objects"></a>Типы сообщений, связанных с объектами пользовательского интерфейса

В следующей таблице показаны типы объектов, с которыми вы работаете, и типы сообщений, связанных с ними.

### <a name="user-interface-objects-and-associated-messages"></a>Объекты пользовательского интерфейса и связанные сообщения

|Идентификатор объекта.|Сообщения|
|---------------|--------------|
|Имя класса, представляющее содержащее окно|Сообщения Windows, соответствующие классу, производному от [CWnd](../../mfc/reference/cwnd-class.md): диалоговое окно, окно, дочернее окно, дочернее окно MDI или окно самого верхнего фрейма.|
|Идентификатор меню или сочетания клавиш|— Сообщение команды (выполняет функцию программы).<br />— UPDATE_COMMAND_UI сообщение (динамически обновляет пункт меню).|
|Идентификатор элемента управления|Управление сообщениями уведомления для выбранного типа элемента управления.|

## <a name="see-also"></a>См. также раздел

[Сопоставление сообщений с функциями](../../mfc/reference/mapping-messages-to-functions.md)<br/>
[Добавление функциональных возможностей с помощью мастеров кода](../../ide/adding-functionality-with-code-wizards-cpp.md)<br/>
[Добавление класса](../../ide/adding-a-class-visual-cpp.md)<br/>
[Добавление функции-члена](../../ide/adding-a-member-function-visual-cpp.md)<br/>
[Добавление переменной-члена](../../ide/adding-a-member-variable-visual-cpp.md)<br/>
[Переопределение виртуальной функции](../../ide/overriding-a-virtual-function-visual-cpp.md)<br/>
[Обработчик сообщений MFC](../../mfc/reference/adding-an-mfc-message-handler.md)<br/>
[Перемещение по структуре класса](../../ide/navigate-code-cpp.md)
