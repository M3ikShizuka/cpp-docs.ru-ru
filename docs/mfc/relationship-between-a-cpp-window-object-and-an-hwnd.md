---
description: 'Дополнительные сведения: связь между объектом окна C++ и HWND'
title: Отношение между объектом окна C++ и HWND
ms.date: 11/19/2018
f1_keywords:
- HWND
helpviewer_keywords:
- Windows window [MFC]
- window objects [MFC], HWND and
- HWND [MFC]
- CWnd class [MFC], HWND
- HWND, window objects [MFC]
ms.assetid: f2e76340-6691-4ee6-9424-0345634a9469
ms.openlocfilehash: bdcf52d2890265b854e3eef7854b489b47eda6a7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97218099"
---
# <a name="relationship-between-a-c-window-object-and-an-hwnd"></a>Отношение между объектом окна C++ и HWND

*Объект* Window — это объект `CWnd` класса C++ (или производного класса), который создается программой напрямую. Это происходит и в ответ на вызовы конструктора и деструктора программы. *Окно* Windows, с другой стороны, является непрозрачным маркером для внутренней структуры данных Windows, которая соответствует окну и потребляет системные ресурсы при их наличии. Окно Windows определяется "обработчиком окна" ( `HWND` ) и создается после того, как `CWnd` объект создан с помощью вызова `Create` функции-члена класса `CWnd` . Окно может быть уничтожено либо вызовом программы, либо действием пользователя. Обработчик окна хранится в переменной-члене *m_hWnd* объекта Window. На следующем рисунке показана связь между объектом окна C++ и окном Windows. Создание Windows рассматривается в разделе [Создание Windows](../mfc/creating-windows.md). Уничтожение Windows рассматривается в разделе [уничтожение объектов Window](../mfc/destroying-window-objects.md).

![Объект окна CWnd и полученное в результате окно](../mfc/media/vc37fj1.gif "Объект окна CWnd и полученное в результате окно") <br/>
Окно "объект окна" и окно "окна"

## <a name="see-also"></a>См. также раздел

[Объекты окна](../mfc/window-objects.md)
