---
description: 'Дополнительные сведения о: использование окна'
title: Использование окна (ATL)
ms.date: 11/04/2016
helpviewer_keywords:
- ATL, windows
- CWindow class, about CWindow class
- windows [C++], ATL
ms.assetid: b3b9cc8e-4287-486b-b080-38852bc2943a
ms.openlocfilehash: fb9f1e03a27ad8b637da30eacbd100daf920cdb4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97157284"
---
# <a name="using-a-window"></a>Использование окна

Класс [CWindow](../atl/reference/cwindow-class.md) позволяет использовать окно. После присоединения окна к `CWindow` объекту можно вызвать `CWindow` методы для управления окном. `CWindow` также содержит оператор HWND для преобразования `CWindow` объекта в HWND. Таким же объектом можно передать `CWindow` объект в любую функцию, для которой требуется маркер окна. Вы можете легко смешивать `CWindow` вызовы методов и вызовы функций Win32 без создания временных объектов.

Поскольку `CWindow` имеет только два элемента данных (маркер окна и измерения по умолчанию), это не приводит к излишней нагрузке на код. Кроме того, многие `CWindow` методы просто упаковывают соответствующие функции API Win32. С помощью `CWindow` элемент HWND автоматически передается функции Win32.

Помимо `CWindow` непосредственного использования, можно также получить от него наследование для добавления данных или кода в класс. Библиотека ATL является производной от трех `CWindow` классов [: квиндовимпл](../atl/implementing-a-window.md), [CDialogImpl](../atl/implementing-a-dialog-box.md)и [кконтаинедвиндовт](../atl/using-contained-windows.md).

## <a name="see-also"></a>См. также раздел

[Классы окон](../atl/atl-window-classes.md)
