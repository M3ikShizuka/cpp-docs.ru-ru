---
description: 'Дополнительные сведения: использование Drop-Down кнопок в элементе управления ToolBar'
title: Использование разворачивающихся кнопок в элементе управления панели инструментов
ms.date: 11/04/2016
f1_keywords:
- TBN_DROPDOWN
- TBSTYLE_EX_DRAWDDARROWS
helpviewer_keywords:
- CToolBarCtrl class [MFC], drop-down buttons
- toolbars [MFC], drop-down buttons
- drop-down buttons in toolbars
- TBSTYLE_EX_DRAWDDARROWS
- TBN_DROPDOWN notification [MFC]
ms.assetid: b859f758-d2f6-40d9-9c26-0ff61993b9b2
ms.openlocfilehash: a37f39397f6b6f66bed1ad1d2fbd9530b55f3d7b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97154465"
---
# <a name="using-drop-down-buttons-in-a-toolbar-control"></a>Использование разворачивающихся кнопок в элементе управления панели инструментов

Помимо стандартных кнопок push-уведомлений, панель инструментов также может содержать кнопки с раскрывающимся списком. Кнопка раскрывающегося списка обычно обозначается наличием присоединенной стрелки вниз.

> [!NOTE]
> Связанная стрелка вниз появится только в том случае, если был установлен расширенный стиль TBSTYLE_EX_DRAWDDARROWS.

Когда пользователь щелкает эту стрелку (или саму кнопку, если отсутствует стрелка), в родительский элемент управления панели инструментов отправляется TBN_DROPDOWN уведомление. Затем можно обработать это уведомление и отобразить всплывающее меню; аналогично поведению Internet Explorer.

В следующей процедуре показано, как реализовать раскрывающуюся кнопку на панели инструментов с всплывающим меню.

### <a name="to-implement-a-drop-down-button"></a>Реализация кнопки раскрывающегося списка

1. После `CToolBarCtrl` создания объекта задайте стиль TBSTYLE_EX_DRAWDDARROWS, используя следующий код:

   [!code-cpp[NVC_MFCControlLadenDialog#36](../mfc/codesnippet/cpp/using-drop-down-buttons-in-a-toolbar-control_1.cpp)]

1. Задайте стиль TBSTYLE_DROPDOWN для всех новых ([инсертбуттон](../mfc/reference/ctoolbarctrl-class.md#insertbutton) или [аддбуттонс](../mfc/reference/ctoolbarctrl-class.md#addbuttons)) или существующих кнопок ([сетбуттонинфо](../mfc/reference/ctoolbarctrl-class.md#setbuttoninfo)), которые будут раскрывающиеся кнопки. В следующем примере показано изменение существующей кнопки в `CToolBarCtrl` объекте.

   [!code-cpp[NVC_MFCControlLadenDialog#37](../mfc/codesnippet/cpp/using-drop-down-buttons-in-a-toolbar-control_2.cpp)]

1. Добавьте обработчик TBN_DROPDOWN в родительский класс объекта панели инструментов.

   [!code-cpp[NVC_MFCControlLadenDialog#38](../mfc/codesnippet/cpp/using-drop-down-buttons-in-a-toolbar-control_3.cpp)]

1. В новом обработчике откройте соответствующее всплывающее меню. В следующем коде демонстрируется один из методов:

   [!code-cpp[NVC_MFCControlLadenDialog#39](../mfc/codesnippet/cpp/using-drop-down-buttons-in-a-toolbar-control_4.cpp)]

## <a name="see-also"></a>См. также раздел

[Использование CToolBarCtrl](../mfc/using-ctoolbarctrl.md)<br/>
[Элементы управления](../mfc/controls-mfc.md)
