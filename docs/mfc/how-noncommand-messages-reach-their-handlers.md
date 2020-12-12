---
description: 'Дополнительные сведения: как Некомандные сообщения достигают обработчиков'
title: Доступ некомандных сообщений к обработчикам
ms.date: 11/04/2016
helpviewer_keywords:
- messages [MFC], routing
- noncommand messages
- Windows messages [MFC], routing
- message handling [MFC], noncommand messages
ms.assetid: e7df8aef-9fae-41f4-9c11-881d8465f602
ms.openlocfilehash: e337a62a731e7ed0832b6cd28d1f56024247c176
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97172821"
---
# <a name="how-noncommand-messages-reach-their-handlers"></a>Доступ некомандных сообщений к обработчикам

В отличие от команд, стандартные сообщения Windows не направляются через цепочку целевых объектов команд, но обычно обрабатываются окном, в которое Windows отправляет сообщение. Окно может быть основным окном фрейма, дочерним окном MDI, стандартным элементом управления, диалоговым окном, представлением или другим видом дочернего окна.

Во время выполнения каждое окно Windows прикрепляется к объекту окна (производному прямо или косвенно от `CWnd` ), который имеет собственную связанную с ним схему сообщений и функции обработчика. Платформа использует схему сообщений, как для команды, чтобы сопоставлять входящие сообщения с обработчиками.

## <a name="see-also"></a>См. также раздел

[Как платформа вызывает обработчик](how-the-framework-calls-a-handler.md)
