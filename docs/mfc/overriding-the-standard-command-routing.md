---
description: 'Дополнительные сведения: переопределение стандартной маршрутизации команд'
title: Переопределение стандартной маршрутизации команд
ms.date: 11/04/2016
helpviewer_keywords:
- MFC, command routing
- command routing [MFC], overriding
- command handling [MFC], routing commands
- overriding, standard command routing
ms.assetid: 872b698a-7432-40c4-9008-68721e8effa5
ms.openlocfilehash: 5241e767beee85f92875128cc5ebccd1a23477f5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97205997"
---
# <a name="overriding-the-standard-command-routing"></a>Переопределение стандартной маршрутизации команд

В редких случаях, когда необходимо реализовать некоторую разновидность маршрутизации стандартной платформы, ее можно переопределить. Идея состоит в том, чтобы изменить маршрутизацию в одном или нескольких классах путем переопределения `OnCmdMsg` в этих классах. Сделайте следующее:

- В классе, который прерывает порядок передачи объекту, не заданному по умолчанию.

- В новом объекте, не используемом по умолчанию, или в целевой команде он может передаваться командам.

Если в маршрутизацию вставляется какой-либо новый объект, его класс должен быть классом целевого объекта. При переопределении версий убедитесь, что `OnCmdMsg` вызывается переопределяемая версия. Примеры см. в описании функции члена [OnCmdMsg](reference/ccmdtarget-class.md#oncmdmsg) класса `CCmdTarget` в *справочнике MFC* и версиях в таких классах, как `CView` и `CDocument` в приведенном исходном коде.

## <a name="see-also"></a>См. также раздел

[Как платформа вызывает обработчик](how-the-framework-calls-a-handler.md)
