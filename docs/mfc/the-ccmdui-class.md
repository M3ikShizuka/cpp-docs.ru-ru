---
description: 'Дополнительные сведения о: класс поддержка CCmdUI'
title: Класс CCmdUI
ms.date: 11/04/2016
helpviewer_keywords:
- updating user interface objects [MFC]
- user interface objects [MFC], updating
- CCmdUI class [MFC], menu updating
- update handlers [MFC]
- toolbars [MFC], updating
ms.assetid: 2f2bae62-8c29-45a4-bbce-490eb01907d5
ms.openlocfilehash: 5fae6d2dda948fd3720a29d502d7f050e388bceb
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97216136"
---
# <a name="the-ccmdui-class"></a>Класс CCmdUI

При передаче команды Update в свой обработчик платформа передает обработчику указатель на `CCmdUI` объект (или на объект `CCmdUI` производного класса). Этот объект представляет элемент меню или кнопку панели инструментов или другой объект пользовательского интерфейса, создавший команду. Обработчик обновлений вызывает функции-члены структуры с `CCmdUI` помощью указателя, чтобы обновить объект пользовательского интерфейса. Например, Вот обработчик обновления для пункта меню Очистить все:

[!code-cpp[NVC_MFCDocView#3](../mfc/codesnippet/cpp/the-ccmdui-class_1.cpp)]

Этот обработчик вызывает `Enable` функцию члена объекта с доступом к элементу меню. `Enable` делает элемент доступным для использования.

## <a name="see-also"></a>См. также раздел

[Руководство. обновление объектов User-Interface](../mfc/how-to-update-user-interface-objects.md)
