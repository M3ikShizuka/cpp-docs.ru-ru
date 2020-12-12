---
description: 'Дополнительные сведения: User-Interface объекты и идентификаторы команд'
title: Объекты пользовательского интерфейса и идентификаторы команд
ms.date: 11/19/2018
helpviewer_keywords:
- keyboard shortcuts, associating with IDs
- MFC, command routing
- toolbar controls [MFC], command ID
- menu items, associating with IDs
- user interface objects [MFC], associating with IDs
- command IDs, user interface objects
- command routing [MFC], MFC
- command handling [MFC], user-interface objects
ms.assetid: 4ea19e9b-ed1e-452e-bd33-7f509107a45b
ms.openlocfilehash: 142b72956e0a1b9e60ef48c7db325cd0ac822444
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97263625"
---
# <a name="user-interface-objects-and-command-ids"></a>Объекты пользовательского интерфейса и идентификаторы команд

Пункты меню, кнопки панели инструментов и сочетания клавиш представляют собой "объекты пользовательского интерфейса", способные создавать команды. Каждый такой объект пользовательского интерфейса имеет идентификатор. Объект пользовательского интерфейса связывается с командой путем присвоения этому же ИДЕНТИФИКАТОРу объекту и команде. Как объясняется в [сообщениях](../mfc/messages.md), команды реализуются как специальные сообщения. На рисунке "команды в платформе" ниже показано, как платформа управляет командами. Когда объект пользовательского интерфейса создает команду, например `ID_EDIT_CLEAR_ALL` , один из объектов в приложении обрабатывает команду (на рисунке ниже, функция объекта документа `OnEditClearAll` вызывается через схему сообщений документа).

![Команды в Framework](../mfc/media/vc385p1.gif "Команды в Framework") <br/>
Команды в Framework

На рисунке ниже показано, как MFC обновляет объекты пользовательского интерфейса, такие как элементы меню и кнопки панели инструментов. Перед выпуском меню или во время цикла бездействия в случае кнопок панели инструментов MFC направляет команду Update. На рисунке ниже объект Document вызывает обработчик команды Update `OnUpdateEditClearAll` для включения или отключения объекта пользовательского интерфейса.

![Обновление команд в Framework](../mfc/media/vc385p2.png "Обновление команд в Framework") <br/>
Обновление команд в платформе

## <a name="see-also"></a>См. также раздел

[Сообщения и команды в платформе](../mfc/messages-and-commands-in-the-framework.md)
