---
description: 'Дополнительные сведения о: использование всплывающих подсказок в объекте CStatusBarCtrl'
title: Использование всплывающих подсказок в объекте CStatusBarCtrl
ms.date: 11/04/2016
helpviewer_keywords:
- tool tips [MFC], using in status bars
- status bars [MFC], tool tips
- CStatusBarCtrl class [MFC], tool tips
ms.assetid: a77597a7-43ef-4b8f-87bc-a8ea1dc63dc3
ms.openlocfilehash: d77610a511698000dc70a1aa1cb1edb22fb3eb7a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97143251"
---
# <a name="using-tooltips-in-a-cstatusbarctrl-object"></a>Использование всплывающих подсказок в объекте CStatusBarCtrl

Чтобы включить подсказки для элемента управления "строка состояния", создайте `CStatusBarCtrl` объект с SBT_TOOLTIPS стилем.

> [!NOTE]
> Если `CStatusBar` для реализации строки состояния используется объект, используйте `CStatusBar::CreateEx` функцию. Он позволяет указать дополнительные стили для внедренного `CStatusBarCtrl` объекта.

После `CStatusBarCtrl` успешного создания объекта используйте [CStatusBarCtrl:: Сеттиптекст](../mfc/reference/cstatusbarctrl-class.md#settiptext) и [CStatusBarCtrl:: жеттиптекст](../mfc/reference/cstatusbarctrl-class.md#gettiptext) , чтобы задать и получить текст подсказки для определенной панели.

Если подсказка задана, она отображается только в том случае, если в части есть значок без текста или если весь текст не может быть отображен внутри части. Всплывающие подсказки не поддерживаются в простом режиме.

## <a name="see-also"></a>См. также раздел

[Использование CStatusBarCtrl](../mfc/using-cstatusbarctrl.md)<br/>
[Элементы управления](../mfc/controls-mfc.md)
