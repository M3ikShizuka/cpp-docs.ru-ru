---
description: 'Дополнительные сведения: установка сочетания клавиш'
title: Задание сочетания клавиш
ms.date: 11/04/2016
helpviewer_keywords:
- keyboard shortcuts [MFC], hot keys
- access keys [MFC], hot keys
- CHotKeyCtrl class [MFC], setting hot key
ms.assetid: 6f3bc141-e346-4dce-9ca7-3e6b2c453f3f
ms.openlocfilehash: fa713be2d478eb18b11dca27558656e5e6993076
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97217189"
---
# <a name="setting-a-hot-key"></a>Задание сочетания клавиш

Приложение может использовать сведения, предоставляемые элементом управления "горячий ключ" ([CHotKeyCtrl](../mfc/reference/chotkeyctrl-class.md)), одним из двух способов:

- Настройте глобальное горячее нажатие клавиши для активации дочернего окна, отправив сообщение [WM_SETHOTKEY](/windows/win32/inputdev/wm-sethotkey) в окно для активации.

- Настройте горячую клавишу для конкретного потока, вызвав функцию Windows [RegisterHotKey](/windows/win32/api/winuser/nf-winuser-registerhotkey).

## <a name="see-also"></a>См. также раздел

[Использование CHotKeyCtrl](../mfc/using-chotkeyctrl.md)<br/>
[Элементы управления](../mfc/controls-mfc.md)
