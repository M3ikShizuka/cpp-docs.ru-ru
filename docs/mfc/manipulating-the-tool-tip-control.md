---
description: Дополнительные сведения об управлении всплывающей подсказкой
title: Управление элементом управления всплывающей подсказки
ms.date: 11/04/2016
helpviewer_keywords:
- CToolTipCtrl class [MFC], manipulating tool tip attributes
- tool tips [MFC], attributes
ms.assetid: 3600afe5-712a-4b56-8456-96e85fe879af
ms.openlocfilehash: f04a2a9fe7d9b32d4b0fab1c6fea0d82f48cbf1a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97281071"
---
# <a name="manipulating-the-tool-tip-control"></a>Управление элементом управления всплывающей подсказки

Класс `CToolTipCtrl` предоставляет группу функций-членов, управляющих различными атрибутами `CToolTipCtrl` объекта и окном подсказки.

Начальные, всплывающие и повторно отображаемые длительности для окон всплывающей подсказки можно задавать и извлекать с помощью вызовов [жетделайтиме](reference/ctooltipctrl-class.md#getdelaytime) и [сетделайтиме](reference/ctooltipctrl-class.md#setdelaytime).

Измените внешний вид окон всплывающей подсказки с помощью следующих функций:

- [Margin](reference/ctooltipctrl-class.md#getmargin) и [сетмаргин](reference/ctooltipctrl-class.md#setmargin) извлекают и устанавливают ширину между границей всплывающей подсказки и текстом всплывающей подсказки.

- [Жетмакстипвидс](reference/ctooltipctrl-class.md#getmaxtipwidth) и [сетмакстипвидс](reference/ctooltipctrl-class.md#setmaxtipwidth) получают и задают максимальную ширину окна подсказки.

- [Жеттипбкколор](reference/ctooltipctrl-class.md#gettipbkcolor) и [сеттипбкколор](reference/ctooltipctrl-class.md#settipbkcolor) извлекает и задает цвет фона для окна подсказки.

- [Жеттиптекстколор](reference/ctooltipctrl-class.md#gettiptextcolor) и [сеттиптекстколор](reference/ctooltipctrl-class.md#settiptextcolor) извлекают и задают цвет текста всплывающей подсказки.

Чтобы элемент управления "Подсказка" мог получать уведомления о важных сообщениях, например WM_LBUTTONXXX сообщениях, необходимо пересылать сообщения в элемент управления "всплывающая подсказка". Лучшим методом для этого ретранслятора является вызов [CToolTipCtrl:: релайевент](reference/ctooltipctrl-class.md#relayevent)в `PreTranslateMessage` функции окна Owner. В следующем примере показан один из возможных методов (при условии, что вызывается элемент управления «подсказка» `m_ToolTip` ):

[!code-cpp[NVC_MFCControlLadenDialog#41](codesnippet/cpp/manipulating-the-tool-tip-control_1.cpp)]

Чтобы немедленно удалить окно подсказки, вызовите функцию-член [POP](reference/ctooltipctrl-class.md#pop) .

## <a name="see-also"></a>См. также раздел

[Использование CToolTipCtrl](using-ctooltipctrl.md)<br/>
[Элементы управления](controls-mfc.md)
