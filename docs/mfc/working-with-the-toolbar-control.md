---
description: 'Дополнительные сведения: работа с элементом управления ToolBar'
title: Работа с элементом управления панели инструментов
ms.date: 11/04/2016
helpviewer_keywords:
- GetToolBarCtrl method [MFC]
- toolbars [MFC], accessing common control
- CToolBarCtrl class [MFC], accessing toolbar
- toolbar controls [MFC], accessing
ms.assetid: b19409d5-3831-42c7-80ae-195c49dc9085
ms.openlocfilehash: bb5b14b35deeff515468a16c82a606704300a395
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97197469"
---
# <a name="working-with-the-toolbar-control"></a>Работа с элементом управления панели инструментов

В этой статье объясняется, как получить доступ к объекту [CToolBarCtrl](../mfc/reference/ctoolbarctrl-class.md) , который является базовым для [CToolBar](../mfc/reference/ctoolbar-class.md) , чтобы лучше управлять панелями инструментов. Это дополнительная тема.

## <a name="procedures"></a>Процедуры

#### <a name="to-access-the-toolbar-common-control-underlying-your-ctoolbar-object"></a>Доступ к панели инструментов общий элемент управления, лежащий в основе объекта CToolBar

1. Вызовите [CToolBar:: жеттулбарктрл](../mfc/reference/ctoolbar-class.md#gettoolbarctrl).

`GetToolBarCtrl` Возвращает ссылку на объект [CToolBarCtrl](../mfc/reference/ctoolbarctrl-class.md) . Можно использовать ссылку для вызова функций элементов класса элемента управления ToolBar.

> [!CAUTION]
> Хотя вызов `CToolBarCtrl` функций **Get** является надежным, будьте внимательны при вызове функций **набора** . Это дополнительная тема. Обычно не требуется доступ к базовому элементу управления ToolBar.

### <a name="what-do-you-want-to-know-more-about"></a>Что вы хотите узнать подробнее

- [Элементы управления (общие элементы управления Windows)](../mfc/controls-mfc.md)

- [Общие сведения о панелях инструментов](../mfc/toolbar-fundamentals.md)

- [Закрепленные и плавающие панели инструментов](../mfc/docking-and-floating-toolbars.md)

- [Динамическое изменение размера панели инструментов](../mfc/docking-and-floating-toolbars.md)

- [Всплывающие подсказки панели инструментов](../mfc/toolbar-tool-tips.md)

- [Обновления строки состояния флиби](../mfc/toolbar-tool-tips.md)

- [Обработка уведомлений всплывающих подсказок](../mfc/handling-tool-tip-notifications.md)

- Классы [CToolBar](../mfc/reference/ctoolbar-class.md) и [CToolBarCtrl](../mfc/reference/ctoolbarctrl-class.md)

- [Обработка уведомлений о настройке](../mfc/handling-customization-notifications.md)

- [Несколько панелей инструментов](../mfc/toolbar-fundamentals.md)

- [Использование старых панелей инструментов](../mfc/using-your-old-toolbars.md)

- [Панели элементов управления](../mfc/control-bars.md)

Общие сведения об использовании стандартных элементов управления Windows см. в разделе [Общие элементы управления](/windows/win32/Controls/common-controls-intro).

## <a name="see-also"></a>См. также раздел

[Реализация панели инструментов MFC](../mfc/mfc-toolbar-implementation.md)
