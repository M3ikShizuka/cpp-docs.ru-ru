---
description: 'Дополнительные сведения о: отсоединение CWnd от HWND'
title: Отсоединение CWnd от HWND
ms.date: 11/04/2016
helpviewer_keywords:
- HWND, detaching CWnd from
- removing HWNDs from CWnds
- CWnd objects [MFC], detaching from HWND
- detaching CWnds from HWNDs
- Detach method (CWnd class)
ms.assetid: 6efadf84-0517-4a3f-acfd-216e088f19c6
ms.openlocfilehash: a3bb1c50b769724ff9ea0f7cdcd2d1fa92cb3a84
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97327807"
---
# <a name="detaching-a-cwnd-from-its-hwnd"></a>Отсоединение CWnd от HWND

Если необходимо обойти объектную `HWND` связь, MFC предоставляет другую функцию- `CWnd` член, [отсоединенную](reference/cwnd-class.md#detach), которая отключает объект окна C++ от окна Windows. Это не дает деструктору уничтожить окно Windows при уничтожении объекта.

## <a name="what-do-you-want-to-know-more-about"></a>Что вы хотите узнать подробнее

- [Создание окон](creating-windows.md)

- [Последовательность уничтожения окна](window-destruction-sequence.md)

- [Выделение и освобождение памяти окна](allocating-and-deallocating-window-memory.md)

## <a name="see-also"></a>См. также раздел

[Объекты окна](window-objects.md)
