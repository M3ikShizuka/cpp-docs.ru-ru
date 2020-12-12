---
description: Дополнительные сведения о последовательности уничтожения окон
title: Последовательность деструкции окна
ms.date: 11/04/2016
helpviewer_keywords:
- destruction, windows
- destroying windows
- sequence [MFC], window destruction
- CWnd objects [MFC], destruction sequence
- sequence [MFC]
- windows [MFC], destroying
ms.assetid: 2d819196-6240-415f-a308-db43745e616c
ms.openlocfilehash: 2ba60f1dcd3668a754bbe4384a6c8cf6b4d541d5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97207687"
---
# <a name="window-destruction-sequence"></a>Последовательность деструкции окна

В платформе MFC, когда пользователь закрывает окно фрейма, обработчик [OnClose](../mfc/reference/cwnd-class.md#onclose) окна по умолчанию вызывает [дестройвиндов](../mfc/reference/cwnd-class.md#destroywindow). Последняя функция-член, вызываемая при уничтожении окна Windows, — это [OnNcDestroy](../mfc/reference/cwnd-class.md#onncdestroy), который выполняет некоторую очистку, вызывает функцию-член [по умолчанию](../mfc/reference/cwnd-class.md#default) для выполнения очистки Windows и, наконец, вызывает виртуальную функцию-член [постнкдестрой](../mfc/reference/cwnd-class.md#postncdestroy). Реализация [CFrameWnd](../mfc/reference/cframewnd-class.md) `PostNcDestroy` удаляет объект окна C++.

## <a name="what-do-you-want-to-know-more-about"></a>Что вы хотите узнать подробнее

- [Выделение и освобождение памяти окна](../mfc/allocating-and-deallocating-window-memory.md)

- [Отсоединение CWnd от HWND](../mfc/detaching-a-cwnd-from-its-hwnd.md)

## <a name="see-also"></a>См. также раздел

[Уничтожение объектов Window](../mfc/destroying-window-objects.md)
