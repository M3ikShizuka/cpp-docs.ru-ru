---
description: 'Дополнительные сведения: уведомления, отправленные элементами управления анимации'
title: Уведомления, отправленные элементами управления "Анимация"
ms.date: 11/04/2016
helpviewer_keywords:
- notifications [MFC], animation controls
- CAnimateCtrl class [MFC], notifications
- controls [MFC], animation
- animation controls [MFC], notifications
ms.assetid: 584f5824-446b-4a1a-85f7-ef61842c8186
ms.openlocfilehash: 17dbd041e1c22b8d6542e64fd8b99d86389ea2d4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97280564"
---
# <a name="notifications-sent-by-animation-controls"></a>Уведомления, отправленные элементами управления "Анимация"

Элемент управления анимации ([CAnimateCtrl](reference/canimatectrl-class.md)) отправляет два разных типа сообщений уведомления. Уведомления отправляются в виде [WM_COMMAND](/windows/win32/menurc/wm-command) сообщений.

[ACN_START](/windows/win32/Controls/acn-start) сообщение отправляется, когда элемент управления анимации начинает воспроизводить клип. [ACN_STOP](/windows/win32/Controls/acn-stop) сообщение отправляется при завершении или остановке воспроизведения клипа элементом управления анимации.

## <a name="see-also"></a>См. также раздел

[Использование CAnimateCtrl](using-canimatectrl.md)<br/>
[Элементы управления](controls-mfc.md)
