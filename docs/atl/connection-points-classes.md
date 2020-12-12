---
description: 'Дополнительные сведения: классы точек подключения'
title: Классы точек подключения (ATL)
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- classes [C++], connection points
- connection points classes
ms.assetid: 076365fa-299a-4dce-84c3-a5dff0e0da1f
ms.openlocfilehash: 28d41f15aeafd98c8c9bcac27fde25d0b2037765
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97148243"
---
# <a name="connection-points-classes"></a>Классы точек подключения

Следующие классы обеспечивают поддержку точек подключения:

- [Иконнектионпоинтконтаинеримпл](../atl/reference/iconnectionpointcontainerimpl-class.md) Реализует контейнер точки соединения.

- [Иконнектионпоинтимпл](../atl/reference/iconnectionpointimpl-class.md) Реализует точку соединения.

- [Ипропертинотифисинккп](../atl/reference/ipropertynotifysinkcp-class.md) Реализует точку соединения, представляющую интерфейс [ипропертинотифисинк](/windows/win32/api/ocidl/nn-ocidl-ipropertynotifysink) .

- [Ккомдинамикункаррай](../atl/reference/ccomdynamicunkarray-class.md) Управляет неограниченными подключениями между точкой подключения и ее приемниками.

- [Ккомункаррай](../atl/reference/ccomunkarray-class.md) Управляет фиксированным числом соединений между точкой подключения и ее приемниками.

- [Кфирепропнотифевент](../atl/reference/cfirepropnotifyevent-class.md) Уведомляет приемник клиента, что свойство объекта изменилось или собирается его изменить.

- [IDispEventImpl](../atl/reference/idispeventimpl-class.md) Обеспечивает поддержку точек соединения для COM-объекта ATL. Эти точки соединения сопоставляются с картой приемника событий, которая предоставляется объектом COM.

- [IDispEventSimpleImpl](../atl/reference/idispeventsimpleimpl-class.md) Работает в сочетании с картой приемника событий в классе для маршрутизации событий в соответствующую функцию обработчика.

## <a name="related-articles"></a>Похожие статьи

[Точки подключения](../atl/atl-connection-points.md)

[Обработка событий и ATL](../atl/event-handling-and-atl.md)

## <a name="see-also"></a>См. также раздел

[Общие сведения о классах](../atl/atl-class-overview.md)<br/>
[Макросы точек подключения](../atl/reference/connection-point-macros.md)<br/>
[Глобальные функции точек подключения](../atl/reference/connection-point-global-functions.md)
