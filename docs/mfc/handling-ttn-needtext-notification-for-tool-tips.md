---
description: Дополнительные сведения см. в статье обработка уведомлений TTN_NEEDTEXT для подсказок
title: Обработка уведомления TTN_NEEDTEXT для всплывающих подсказок
ms.date: 11/04/2016
f1_keywords:
- TTN_NEEDTEXT
helpviewer_keywords:
- TTN_NEEDTEXT message [MFC]
- notifications [MFC], tool tips
- tool tips [MFC], notifications
ms.assetid: d0370a65-21ba-4676-bcc5-8cf851bbb15c
ms.openlocfilehash: 793f6c42e0e43c341884b999e5e1aed0be448b00
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97326422"
---
# <a name="handling-ttn_needtext-notification-for-tool-tips"></a>Обработка уведомления TTN_NEEDTEXT для всплывающих подсказок

В рамках [включения советов](enabling-tool-tips.md)вы обрабатываете **TTN_NEEDTEXT** сообщение, добавив следующую запись в схему сообщений окна владельца:

[!code-cpp[NVC_MFCControlLadenDialog#40](codesnippet/cpp/handling-ttn-needtext-notification-for-tool-tips_1.cpp)]

*мемберфксн*<br/>
Функция-член, вызываемая, когда для этой кнопки требуется текст.

Обратите внимание, что идентификатор подсказки всегда равен 0.

Объявите функцию обработчика в определении класса следующим образом:

[!code-cpp[NVC_MFCControlLadenDialog#53](codesnippet/cpp/handling-ttn-needtext-notification-for-tool-tips_2.h)]

Ниже перечислены параметры с курсивом.

*id*<br/>
Идентификатор элемента управления, отправившего уведомление. Не используется. Идентификатор элемента управления берется из структуры **NMHDR** .

*пнмхдр*<br/>
Указатель на структуру [нмттдиспинфо](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfow) . Эта структура также обсуждается далее в [структуре ToolTipText](tooltiptext-structure.md).

*пресулт*<br/>
Указатель на код результата, который можно задать перед возвратом. Обработчики **TTN_NEEDTEXT** могут игнорировать параметр *пресулт* .

В качестве примера обработчика уведомлений представления формы:

[!code-cpp[NVC_MFCControlLadenDialog#54](codesnippet/cpp/handling-ttn-needtext-notification-for-tool-tips_3.cpp)]

Вызов `EnableToolTips` (этот фрагмент взят из `OnInitDialog` ):

[!code-cpp[NVC_MFCControlLadenDialog#55](codesnippet/cpp/handling-ttn-needtext-notification-for-tool-tips_4.cpp)]

## <a name="see-also"></a>См. также раздел

[Всплывающие подсказки в Windows, не являющиеся производными от CFrameWnd](tool-tips-in-windows-not-derived-from-cframewnd.md)
