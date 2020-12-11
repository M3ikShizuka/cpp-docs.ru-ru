---
description: 'Дополнительные сведения: обработка сообщений уведомлений в элементах управления "список"'
title: Обработка уведомляющих сообщений в элементах управления списками
ms.date: 11/04/2016
helpviewer_keywords:
- processing notifications [MFC]
- CListCtrl class [MFC], processing notifications
ms.assetid: 1f0e296e-d2a3-48fc-ae38-51d7fb096f51
ms.openlocfilehash: b761f5213a73ce31484a7a252b9b441da2fe154d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97154803"
---
# <a name="processing-notification-messages-in-list-controls"></a>Обработка уведомляющих сообщений в элементах управления списками

Когда пользователи щелкают заголовки столбцов, перетаскивать значки, изменять метки и т. д., элемент управления "список" ([CListCtrl](../mfc/reference/clistctrl-class.md)) отправляет сообщения уведомления в родительское окно. Обрабатывайте эти сообщения, если требуется сделать что-нибудь в ответе. Например, когда пользователь щелкает заголовок столбца, может потребоваться отсортировать элементы по содержимому столбца, выбранному щелчком мыши, как в Microsoft Outlook.

Обработка WM_NOTIFY сообщений из элемента управления "список" в классе представления или диалогового окна. Используйте [мастер классов](reference/mfc-class-wizard.md) для создания функции обработчика [ончилднотифи](../mfc/reference/cwnd-class.md#onchildnotify) с инструкцией Switch, основанной на том, какое сообщение уведомления обрабатывается.

Список уведомлений, которые элемент управления "список" может отправить в родительское окно, см. в подразделе [ссылка на элемент управления](/windows/win32/Controls/list-view-control-reference) списком в Windows SDK.

## <a name="see-also"></a>См. также раздел

[Использование CListCtrl](../mfc/using-clistctrl.md)<br/>
[Элементы управления](../mfc/controls-mfc.md)
