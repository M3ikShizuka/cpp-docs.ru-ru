---
description: Дополнительные сведения см. в статье управляющие сообщения с уведомлениями в виде дерева
title: Уведомляющие сообщения древовидного элемента управления
ms.date: 11/04/2016
helpviewer_keywords:
- notifications [MFC], tree controls
- messages [MFC], notification
- CTreeCtrl class [MFC], notifications
- notifications [MFC], CTreeCtrl
- tree controls [MFC], notification messages
ms.assetid: ac7013b4-91dd-4668-bd75-439ca0680ef9
ms.openlocfilehash: 899b6469a2de9a076dd33e62c5023f502448d45f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97263989"
---
# <a name="tree-control-notification-messages"></a>Уведомляющие сообщения древовидного элемента управления

Элемент управления "дерево" ([CTreeCtrl](../mfc/reference/ctreectrl-class.md)) отправляет следующие сообщения уведомлений как WM_NOTIFY сообщения:

|Сообщение уведомления|Описание|
|--------------------------|-----------------|
|TVN_BEGINDRAG|Сигнализирует о начале операции перетаскивания|
|TVN_BEGINLABELEDIT|Сигнализирует начало редактирования метки на месте|
|TVN_BEGINRDRAG|Сигнализирует о начале операции перетаскивания с помощью правой кнопки мыши|
|TVN_DELETEITEM|Сообщает об удалении определенного элемента|
|TVN_ENDLABELEDIT|Сообщает об окончании редактирования метки|
|TVN_GETDISPINFO|Запрашивает сведения, необходимые элементу управления "дерево" для вывода элемента|
|TVN_ITEMEXPANDED|Сообщает, что список дочерних элементов родительского элемента был развернут или свернут|
|TVN_ITEMEXPANDING|Сигнализирует, что список дочерних элементов родительского элемента будет развернут или свернут|
|TVN_KEYDOWN|Сигнализирует о событии клавиатуры|
|TVN_SELCHANGED|Сигнализирует, что выделение изменилось с одного элемента на другой|
|TVN_SELCHANGING|Сигнализирует, что выбор будет изменен с одного элемента на другой|
|TVN_SETDISPINFO|Уведомление для обновления сведений, сохраняемых для элемента|

## <a name="see-also"></a>См. также раздел

[Использование CTreeCtrl](../mfc/using-ctreectrl.md)<br/>
[Элементы управления](../mfc/controls-mfc.md)
