---
description: 'Дополнительные сведения: обработка сообщений с уведомлениями элемента управления "Вкладка"'
title: Обработка уведомляющих сообщений элемента управления "Вкладка"
ms.date: 11/04/2016
helpviewer_keywords:
- notifications [MFC], tab controls
- CTabCtrl class [MFC], processing notifications
- notifications [MFC], processing in CTabCtrl
- processing notifications [MFC]
- tab controls [MFC], processing notifications
ms.assetid: 758ccb7a-9e73-48f8-9073-23f7cb09918c
ms.openlocfilehash: f5d81437b566143e2fc7cb1e0f275c0f9e9993de
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97154725"
---
# <a name="processing-tab-control-notification-messages"></a>Обработка уведомляющих сообщений элемента управления "Вкладка"

Когда пользователи щелкают вкладки или кнопки, элемент управления "Вкладка" ([CTabCtrl](../mfc/reference/ctabctrl-class.md)) отправляет сообщения уведомления в родительское окно. Обрабатывайте эти сообщения, если требуется сделать что-нибудь в ответе. Например, когда пользователь щелкает вкладку, может потребоваться предварительно установить контрольные данные на странице перед ее отображением.

Обработка WM_NOTIFY сообщений из элемента управления "Вкладка" в классе представления или диалогового окна. Используйте [мастер классов](reference/mfc-class-wizard.md) для создания функции обработчика [ончилднотифи](../mfc/reference/cwnd-class.md#onchildnotify) с инструкцией Switch, основанной на том, какое сообщение уведомления обрабатывается. Список уведомлений, которые элемент управления "Вкладка" может отправить в родительское окно, см. в разделе " **уведомления** [" Справочника по элементу управления Tab](/windows/win32/controls/tab-control-reference) в Windows SDK.

## <a name="see-also"></a>См. также раздел

[Использование CTabCtrl](../mfc/using-ctabctrl.md)<br/>
[Элементы управления](../mfc/controls-mfc.md)
