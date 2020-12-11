---
description: 'Дополнительные сведения: классы окон кадров (архитектура)'
title: Классы окна фрейма (архитектура)
ms.date: 11/04/2016
helpviewer_keywords:
- frame window classes [MFC], document/view architecture
ms.assetid: 5da01fb4-f531-46cc-914f-e422e4f07f5d
ms.openlocfilehash: 045108cd1e45325cf6069b5d8259ffab9abb0c2e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97155037"
---
# <a name="frame-window-classes-architecture"></a>Классы окна фрейма (архитектура)

В архитектуре "документ-представление" окна фрейма — это окна, содержащие окно представления. Они также поддерживают наличие прикрепленных к ним панелей управления.

В приложениях с многодокументным интерфейсом (MDI) основное окно является производным от `CMDIFrameWnd` . Он косвенно содержит кадры документов, которые являются `CMDIChildWnd` объектами. `CMDIChildWnd`Объекты, в свою очередь, содержат представления документов.

В приложениях с одним документом (SDI) главное окно, производное от `CFrameWnd` , содержит представление текущего документа.

[CFrameWnd](reference/cframewnd-class.md)<br/>
Базовый класс для основного окна фрейма приложения SDI. Кроме того, базовый класс для всех других классов окон фрейма.

[CMDIFrameWnd](reference/cmdiframewnd-class.md)<br/>
Базовый класс для главного окна фрейма приложения MDI.

[CMDIChildWnd](reference/cmdichildwnd-class.md)<br/>
Базовый класс для окон фрейма документа приложения MDI.

[COleIPFrameWnd](reference/coleipframewnd-class.md)<br/>
Предоставляет окно фрейма для представления, когда серверный документ редактируется на месте.

## <a name="see-also"></a>См. также раздел

[Общие сведения о классах](class-library-overview.md)
