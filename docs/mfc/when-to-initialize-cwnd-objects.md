---
description: 'Дополнительные сведения о: когда следует инициализировать объекты CWnd'
title: Время инициализации объектов CWnd
ms.date: 11/04/2016
helpviewer_keywords:
- window objects [MFC], when to initialize CWnd
- initializing CWnd objects [MFC]
- initializing objects [MFC], CWnd
- CWnd objects [MFC], when HWND is attached
- HWND, when attached to CWnd object
- CWnd objects [MFC], when to initialize
ms.assetid: 4d31bcb1-73db-4f2f-b71c-89b087569a10
ms.openlocfilehash: 89d40b826507574fddd41364ac6cecc526663519
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97142770"
---
# <a name="when-to-initialize-cwnd-objects"></a>Время инициализации объектов CWnd

Нельзя создавать собственные дочерние окна или вызывать функции API Windows в конструкторе `CWnd` объекта, производного от. Это происходит потому, что `HWND` `CWnd` объект для объекта еще не создан. Большая часть инициализации Windows, например добавление дочерних окон, должна выполняться обработчиком сообщений [OnCreate](../mfc/reference/cwnd-class.md#oncreate) .

## <a name="what-do-you-want-to-know-more-about"></a>Что вы хотите узнать подробнее

- [Создание окон фрейма документа](../mfc/creating-document-frame-windows.md)

- [Создание документа или представления](../mfc/document-view-creation.md)

## <a name="see-also"></a>См. также раздел

[Использование окон фрейма](../mfc/using-frame-windows.md)
