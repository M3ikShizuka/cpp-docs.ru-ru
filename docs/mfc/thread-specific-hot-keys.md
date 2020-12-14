---
description: 'Дополнительные сведения: Thread-Specific горячие клавиши'
title: Сочетания клавиш для определенного потока
ms.date: 11/04/2016
helpviewer_keywords:
- CHotKeyCtrl class [MFC], thread-specific hot keys
- keyboard shortcuts [MFC], hot keys
- threading [MFC], hot keys in CHotKeyCtrl
- access keys [MFC], hot keys
ms.assetid: b6021274-1498-483f-bcbf-ba5723547cc8
ms.openlocfilehash: 352d39b801d7e6dcecfbf27d841d6977d3666138
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97216123"
---
# <a name="thread-specific-hot-keys"></a>Сочетания клавиш для определенного потока

Приложение устанавливает горячую клавишу для конкретного потока ([CHotKeyCtrl](../mfc/reference/chotkeyctrl-class.md)) с помощью функции Windows `RegisterHotKey` . Когда пользователь нажимает на специальную клавишу для конкретного потока, Windows отправляет сообщение [WM_HOTKEY](/windows/win32/inputdev/wm-hotkey) в начало очереди сообщений определенного потока. Сообщение WM_HOTKEY содержит виртуальный код ключа, состояние сдвига и определяемый пользователем идентификатор определенного сочетания клавиш. Список стандартных виртуальных клавиш см. в разделе Winuser. h. Дополнительные сведения об этом методе см. в разделе [RegisterHotKey](/windows/win32/api/winuser/nf-winuser-registerhotkey).

Обратите внимание, что флаги состояния сдвига, используемые в вызове `RegisterHotKey` , не совпадают с параметрами [,](../mfc/reference/chotkeyctrl-class.md#gethotkey) возвращаемыми функцией члена функции. перед вызовом необходимо преобразовать эти флаги `RegisterHotKey` .

## <a name="see-also"></a>См. также раздел

[Использование CHotKeyCtrl](../mfc/using-chotkeyctrl.md)<br/>
[Элементы управления](../mfc/controls-mfc.md)
