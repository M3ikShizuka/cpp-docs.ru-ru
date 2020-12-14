---
description: 'Дополнительные сведения о: использование CStatusBarCtrl для создания объекта CStatusBarCtrl'
title: Использование CStatusBarCtrl для создания объекта CStatusBarCtrl
ms.date: 11/04/2016
helpviewer_keywords:
- status bar controls [MFC], creating
- CStatusBarCtrl class [MFC], creating
ms.assetid: 365c2b65-12de-49e6-9a2e-416c6ee10d60
ms.openlocfilehash: 0b76065ce4e90600bdec7e4f4a89ee2c5bb14085
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97202383"
---
# <a name="using-cstatusbarctrl-to-create-a-cstatusbarctrl-object"></a>Использование CStatusBarCtrl для создания объекта CStatusBarCtrl

Ниже приведен пример типичного использования [CStatusBarCtrl](../mfc/reference/cstatusbarctrl-class.md):

### <a name="to-use-a-status-bar-control-with-parts"></a>Использование элемента управления "строка состояния" с частями

1. Создайте `CStatusBarCtrl` объект.

1. Вызовите [сетминхеигхт](../mfc/reference/cstatusbarctrl-class.md#setminheight) , если хотите задать минимальную высоту области рисования элемента управления "строка состояния".

1. Вызовите [сетбкколор](../mfc/reference/cstatusbarctrl-class.md#setbkcolor) , чтобы задать цвет фона для элемента управления "строка состояния".

1. Вызовите [сетпартс](../mfc/reference/cstatusbarctrl-class.md#setparts) , чтобы задать количество частей в элементе управления "строка состояния" и координату правого края каждой части.

1. Вызовите [SetText](../mfc/reference/cstatusbarctrl-class.md#settext) , чтобы задать текст в заданной части элемента управления "строка состояния". Сообщение сделает недействительным измененную часть элемента управления, что привело бы к отображению нового текста, когда элемент управления затем получает сообщение WM_PAINT.

В некоторых случаях в строке состояния должна отображаться только строка текста. В этом случае выполните вызов [сетсимпле](../mfc/reference/cstatusbarctrl-class.md#setsimple). При этом элемент управления "строка состояния" помещается в режим "простой", в котором отображается одна строка текста.

## <a name="see-also"></a>См. также раздел

[Использование CStatusBarCtrl](../mfc/using-cstatusbarctrl.md)<br/>
[Элементы управления](../mfc/controls-mfc.md)
