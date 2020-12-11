---
description: 'Дополнительные сведения: перетаскивание файлов в окне фрейма'
title: Перетаскивание файлов в окне фрейма
ms.date: 11/04/2016
helpviewer_keywords:
- drag and drop [MFC], files
- drag and drop [MFC], File Manager
- Windows Explorer [MFC]
- File Manager drag and drop support [MFC]
- files [MFC], drag and drop
- frame windows [MFC], dragging and dropping files in
- drag and drop [MFC], Windows Explorer
ms.assetid: 85560fe9-121b-4105-bd7b-216b966e19fa
ms.openlocfilehash: dafbeca8b74ee07c80315c15ab93097977125d89
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97159951"
---
# <a name="dragging-and-dropping-files-in-a-frame-window"></a>Перетаскивание файлов в окне фрейма

Окно фрейма управляет связью с помощью проводника или диспетчера файлов.

Добавив несколько вызовов инициализации в Переопределение `CWinApp` функции-члена `InitInstance` , как описано в разделе ["CWinApp: класс приложения"](cwinapp-the-application-class.md), можно настроить окно фрейма на непрямое открытие файлов, которые перетаскиваются из проводника или из диспетчера файлов и удаляются в окне фрейма. См. раздел [перетаскивание диспетчера файлов](special-cwinapp-services.md).

## <a name="see-also"></a>См. также раздел

[Использование окон фрейма](using-frame-windows.md)
