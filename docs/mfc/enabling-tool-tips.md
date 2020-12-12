---
description: Дополнительные сведения см. в статье Включение всплывающих подсказок
title: Включение всплывающих подсказок
ms.date: 11/04/2016
helpviewer_keywords:
- initializing tool tips [MFC]
- enabling tool tips [MFC]
- tool tips [MFC], initializing
- tool tips [MFC], enabling
ms.assetid: 06b7c889-7722-4ce6-8b88-9efa50fe6369
ms.openlocfilehash: 677d2cc071e87f62f9bd2e700d8fdba166dfdee7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97290951"
---
# <a name="enabling-tool-tips"></a>Включение всплывающих подсказок

Можно включить поддержку всплывающих подсказок для дочерних элементов управления окна (таких как элементы управления в представлении формы или диалоговом окне).

### <a name="to-enable-tool-tips-for-the-child-controls-of-a-window"></a>Включение всплывающих подсказок для дочерних элементов управления окна

1. Вызовите `EnableToolTips` для окна, для которого необходимо предоставить подсказки.

1. Укажите строку для каждого элемента управления в обработчике [уведомлений TTN_NEEDTEXT](handling-ttn-needtext-notification-for-tool-tips.md) . Обработчик находится в схеме сообщений окна, содержащего дочерние элементы управления (например, класс представления формы). Этот обработчик должен вызвать функцию, которая идентифицирует элемент управления и задает **псзтекст** для указания текста, используемого элементом управления "Подсказка".

## <a name="see-also"></a>См. также раздел

[Всплывающие подсказки в Windows, не являющиеся производными от CFrameWnd](tool-tips-in-windows-not-derived-from-cframewnd.md)
