---
description: Дополнительные сведения о уничтожении объектов Window
title: Уничтожение объектов окон
ms.date: 11/04/2016
helpviewer_keywords:
- frame windows [MFC], destroying
- window objects [MFC], deleting
- window objects [MFC], destroying
- window objects [MFC], removing
ms.assetid: 3241fea0-c614-4a25-957d-20f21bd5fd0c
ms.openlocfilehash: c2837ba6b9f568d7f6ab0175ae3ad99c31ccdc7e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97327815"
---
# <a name="destroying-window-objects"></a>Уничтожение объектов окон

Будьте осторожны с собственными дочерними окнами, чтобы уничтожить объект окна C++, когда пользователь завершит работу с окном. Если эти объекты не уничтожаются, приложение не будет восстанавливать память. К счастью, платформа управляет уничтожением окна, а также созданием окон фрейма, представлений и диалогов. Если вы создаете дополнительные окна, вы несете ответственность за их уничтожение.

## <a name="what-do-you-want-to-know-more-about"></a>Что вы хотите узнать подробнее

- [Последовательность уничтожения окна](window-destruction-sequence.md)

- [Выделение и освобождение памяти окна](allocating-and-deallocating-window-memory.md)

- [Отсоединение CWnd от HWND](detaching-a-cwnd-from-its-hwnd.md)

- [Общая последовательность создания окна](general-window-creation-sequence.md)

- [Уничтожение окон фрейма](destroying-frame-windows.md)

## <a name="see-also"></a>См. также раздел

[Объекты окна](window-objects.md)
