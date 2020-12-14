---
description: 'Дополнительные сведения: обработчики для команд и уведомления об управлении'
title: Обработчики для команд и уведомлений элементов управления
ms.date: 11/04/2016
helpviewer_keywords:
- commands [MFC], handlers for
- functions [MFC], handler
- handlers [MFC]
- controls [MFC], notifications
- handlers [MFC], control notification [MFC]
- notifications [MFC], handlers for control
- handlers [MFC], command
ms.assetid: 20f57f4a-f577-4c09-80a2-43faf32a1c2e
ms.openlocfilehash: 1e5e3284d5898d1e6349765dc7a1bcdc864c80ef
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97189188"
---
# <a name="handlers-for-commands-and-control-notifications"></a>Обработчики для команд и уведомлений элементов управления

Нет обработчиков по умолчанию для команд или сообщений уведомления об управлении. Поэтому вы привязаны только по соглашению в именовании обработчиков для этих категорий сообщений. При сопоставлении команды или уведомления элемента управления с обработчиком, [мастер классов](reference/mfc-class-wizard.md) предлагает имя на основе идентификатора команды или кода уведомления элемента управления. Вы можете принять предложенное имя, изменить его или заменить.

Соглашение предполагает, что вы наименают обработчики в обеих категориях для объекта пользовательского интерфейса, который они представляют. Таким же обработчиком команды Cut в меню Правка может быть присвоено имя

[!code-cpp[NVC_MFCMessageHandling#4](codesnippet/cpp/handlers-for-commands-and-control-notifications_1.h)]

Поскольку команда Cut так часто реализуется в приложениях, платформа определяет идентификатор команды для команды Cut как **ID_EDIT_CUT**. Список всех предопределенных идентификаторов команд см. в файле AFXRES. H. Дополнительные сведения см. в разделе [стандартные команды](standard-commands.md).

Кроме того, соглашение предлагает обработчик для сообщения **BN_CLICKED** уведомления на кнопке с надписью "Моя кнопка" может называться

[!code-cpp[NVC_MFCMessageHandling#5](codesnippet/cpp/handlers-for-commands-and-control-notifications_2.h)]

Этой команде можно назначить идентификатор **IDC_MY_BUTTON** так как он эквивалентен объекту пользовательского интерфейса, определяемому приложением.

Обе категории сообщений не имеют аргументов и не возвращают значения.

## <a name="see-also"></a>См. также раздел

[Объявление функций обработчика сообщений](declaring-message-handler-functions.md)
