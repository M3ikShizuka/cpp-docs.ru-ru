---
description: Дополнительные сведения о том, что такое Windows Frame
title: Функция окон фрейма
ms.date: 11/04/2016
helpviewer_keywords:
- frame windows [MFC], about frame windows
- frame windows [MFC], tasks
- MFC, frame windows
ms.assetid: 1148a952-6786-4622-b5a8-68a2d7eae584
ms.openlocfilehash: 8f70bbe55b15310133688079236fe57459679090
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97142835"
---
# <a name="what-frame-windows-do"></a>Функция окон фрейма

Помимо простой кадрирования представления, окна фрейма отвечают за множество задач, участвующих в координации кадра с его представлением и с приложением. [CMDIFrameWnd](../mfc/reference/cmdiframewnd-class.md) и [CMDIChildWnd](../mfc/reference/cmdichildwnd-class.md) наследуют от [CFrameWnd](../mfc/reference/cframewnd-class.md), поэтому у них есть возможности, а `CFrameWnd` также новые возможности, которые они добавляют. Примерами дочерних окон являются представления, элементы управления, такие как кнопки и списки, а также панели элементов управления, включая панели инструментов, строки состояния и диалоговые панели.

Окно фрейма отвечает за управление макетом дочерних окон. В платформе MFC окно фрейма размещает все панели управления, представления и другие дочерние окна в своей клиентской области.

Окно фрейма также пересылает команды в свои представления и может отвечать на сообщения уведомления от окон управления.

## <a name="what-do-you-want-to-know-more-about"></a>Что вы хотите узнать подробнее

- [Панели элементов управления (их размер в окне фрейма)](../mfc/control-bars.md)

- [Управление меню, панелями управления и ускорителями (их размещение в окне фрейма)](../mfc/managing-menus-control-bars-and-accelerators.md)

- [Маршрутизация команд (из окна фрейма в представление и другие целевые объекты команды)](../mfc/command-routing.md)

- [Документирование архитектуры/Виев](../mfc/document-view-architecture.md)

- [Панели элементов управления](../mfc/control-bars.md)

- [Элементы управления](../mfc/controls-mfc.md)

## <a name="see-also"></a>См. также раздел

[Окна фрейма](../mfc/frame-windows.md)
