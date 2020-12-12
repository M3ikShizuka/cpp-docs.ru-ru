---
description: 'Дополнительные сведения: целевые объекты команды'
title: Цели команды
ms.date: 11/04/2016
helpviewer_keywords:
- command targets
- command mapping
- messages, command [MFC]
- command routing [MFC], command targets
ms.assetid: b0f784e5-c6dc-4391-9e71-aa7b7dcbe9f0
ms.openlocfilehash: b7be03282400c2d3a0dcf5eb0d24a0b06456ebca
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97206257"
---
# <a name="command-targets"></a>Цели команды

Команды на рисунке [в платформе](user-interface-objects-and-command-ids.md) показывают соединение между объектом пользовательского интерфейса, например пунктом меню, и функцией обработчика, которая вызывается платформой для выполнения результирующей команды при щелчке объекта.

Windows отправляет сообщения, которые не являются командными сообщениями непосредственно в окно, обработчик которого для сообщения вызывается. Однако платформа направляет команды на ряд объектов-кандидатов, именуемых "целевыми объектами команды", одна из которых обычно вызывает обработчик для команды. Функции обработчика работают одинаково для обеих команд и стандартных сообщений Windows, но механизмы, с помощью которых они вызываются, отличаются, как описано в [описании того, как платформа вызывает обработчик](how-the-framework-calls-a-handler.md).

## <a name="see-also"></a>См. также раздел

[Сообщения и команды в платформе](messages-and-commands-in-the-framework.md)
