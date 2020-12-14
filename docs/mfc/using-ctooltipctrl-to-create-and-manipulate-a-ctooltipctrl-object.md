---
description: 'Дополнительные сведения: использование CToolTipCtrl для создания объекта CToolTipCtrl и управления им'
title: Использование CToolTipCtrl для создания объекта CToolTipCtrl и управления им
ms.date: 11/04/2016
helpviewer_keywords:
- tool tips [MFC], creating
- CToolTipCtrl class [MFC], using
ms.assetid: 0a34583f-f66d-46a1-a239-31b80ea395ad
ms.openlocfilehash: 363d46ce078b71cf88d742ae390ab674a73ab935
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97202344"
---
# <a name="using-ctooltipctrl-to-create-and-manipulate-a-ctooltipctrl-object"></a>Использование CToolTipCtrl для создания объекта CToolTipCtrl и управления им

Ниже приведен пример использования [CToolTipCtrl](../mfc/reference/ctooltipctrl-class.md) .

### <a name="to-create-and-manipulate-a-ctooltipctrl"></a>Создание CToolTipCtrl и работа с ними

1. Создайте `CToolTipCtrl` объект.

1. Вызовите [CREATE](../mfc/reference/ctooltipctrl-class.md#create) , чтобы создать общий элемент управления всплывающей подсказки Windows и присоединить его к `CToolTipCtrl` объекту.

1. Вызовите [аддтул](../mfc/reference/ctooltipctrl-class.md#addtool) , чтобы зарегистрировать инструмент с помощью элемента управления "Подсказка", чтобы информация, хранящаяся в подсказке, отображалась, когда курсор находится на инструменте.

1. Вызовите [сеттулинфо](../mfc/reference/ctooltipctrl-class.md#settoolinfo) , чтобы задать сведения, которые поддерживает всплывающая подсказка для средства.

1. Вызовите [сеттулрект](../mfc/reference/ctooltipctrl-class.md#settoolrect) , чтобы задать новый ограничивающий прямоугольник для инструмента.

1. Вызовите [HitTest](../mfc/reference/ctooltipctrl-class.md#hittest) , чтобы проверить точку, чтобы определить, находится ли он в ограничивающем прямоугольнике данного инструмента, и, если это так, получить сведения о средстве.

1. Вызовите [жеттулкаунт](../mfc/reference/ctooltipctrl-class.md#gettoolcount) , чтобы получить количество средств, зарегистрированных с помощью элемента управления "Подсказка".

## <a name="see-also"></a>См. также раздел

[Использование CToolTipCtrl](../mfc/using-ctooltipctrl.md)<br/>
[Элементы управления](../mfc/controls-mfc.md)
