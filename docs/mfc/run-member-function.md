---
description: Дополнительные сведения о выполнении функции члена
title: Выполнение функции-члена
ms.date: 11/04/2016
helpviewer_keywords:
- WinMain method [MFC]
ms.assetid: 24ab7597-2354-495b-9a20-2c8ccc7385b3
ms.openlocfilehash: ae67c6b02344a65735ce06775b1d1788d1dabf2c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97217826"
---
# <a name="run-member-function"></a>Выполнение функции-члена

Приложение платформы тратит большую часть времени на функцию-член [Run](../mfc/reference/cwinapp-class.md#run) класса [CWinApp](../mfc/reference/cwinapp-class.md). После инициализации `WinMain` вызывает метод, `Run` чтобы обработать цикл обработки сообщений.

`Run` циклический перебор цикла обработки сообщений, проверка очереди сообщений на наличие доступных сообщений. Если сообщение доступно, `Run` отправляет его для действия. Если нет доступных сообщений, что часто имеет значение true, `Run` вызывается `OnIdle` для выполнения любой обработки, которая может потребоваться вам или платформе. Если нет сообщений и нет бездействующей обработки, приложение ждет, пока что-то не получится. При завершении работы приложения `Run` вызывает метод `ExitInstance` . На рисунке в [функции участника OnIdle](../mfc/onidle-member-function.md) показана последовательность действий в цикле обработки сообщений.

Отправка сообщений зависит от типа сообщения. Дополнительные сведения см. [в разделе сообщения и команды в платформе](../mfc/messages-and-commands-in-the-framework.md).

## <a name="see-also"></a>См. также раздел

[CWinApp: класс Application](../mfc/cwinapp-the-application-class.md)
