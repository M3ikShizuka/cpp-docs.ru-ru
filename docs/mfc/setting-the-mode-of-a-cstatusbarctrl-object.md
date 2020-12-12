---
description: 'Дополнительные сведения: Установка режима для объекта CStatusBarCtrl'
title: Установка режима объекта CStatusBarCtrl
ms.date: 11/04/2016
helpviewer_keywords:
- simple mode and status bar controls
- IsSimple method, using
- SetSimple method [MFC]
- status bar controls [MFC], simple and nonsimple modes
- non-simple mode and status bar controls
- CStatusBarCtrl class [MFC], simple and nonsimple modes
ms.assetid: ca6076e5-1501-4e33-8d35-9308941e46c0
ms.openlocfilehash: 46a87c17c68059e1d12476f4963f159cd2915824
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97217111"
---
# <a name="setting-the-mode-of-a-cstatusbarctrl-object"></a>Установка режима объекта CStatusBarCtrl

Существует два режима для `CStatusBarCtrl` объекта: простой и непростой. В большинстве случаев элемент управления "строка состояния" будет содержать одну или несколько частей, а также текст и, возможно, значок или значки. Это называется непростым режимом. Дополнительные сведения об этом режиме см. [в разделе Инициализация частей объекта CStatusBarCtrl](../mfc/initializing-the-parts-of-a-cstatusbarctrl-object.md).

Однако бывают случаи, когда нужно отобразить только одну строку текста. В этом случае достаточно простого режима для ваших нужд. Чтобы изменить режим `CStatusBarCtrl` объекта на простой, выполните вызов функции-члена [сетсимпле](../mfc/reference/cstatusbarctrl-class.md#setsimple) . Когда элемент управления "строка состояния" находится в простом режиме, задайте текст, вызвав `SetText` функцию-член, передав 255 в качестве значения параметра *нпане* .

Для определения режима, в котором находится объект, можно использовать функцию [простое_имя](../mfc/reference/cstatusbarctrl-class.md#issimple) `CStatusBarCtrl` .

> [!NOTE]
> Если объект строки состояния изменяется с непростого на простой или наоборот, то окно немедленно перерисовывается и, если применимо, все определенные части автоматически восстанавливаются.

## <a name="see-also"></a>См. также раздел

[Использование CStatusBarCtrl](../mfc/using-cstatusbarctrl.md)<br/>
[Элементы управления](../mfc/controls-mfc.md)
