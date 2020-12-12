---
description: Дополнительные сведения см. в статье классы точек подключения ATL.
title: Классы точки подключения библиотеки ATL
ms.date: 11/04/2016
helpviewer_keywords:
- CFirePropNotifyEvent class, connection point classes
- connection points [C++], ATL classes
- ATL, connection points
- CComDynamicUnkArray class, connection point classes
- CFirePropNotifyEvent class
- CComUnkArray class, connection point classes
ms.assetid: 9582ba71-7ace-4df4-9c9b-1b0636953efc
ms.openlocfilehash: af3b52715d7aeca13a711557bdba2c9428d4bff5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97165853"
---
# <a name="atl-connection-point-classes"></a>Классы точки подключения библиотеки ATL

ATL использует следующие классы для поддержки точек подключения:

- [Иконнектионпоинтимпл](../atl/reference/iconnectionpointimpl-class.md) реализует точку подключения. Идентификатор IID исходящего интерфейса, который он представляет, передается как параметр шаблона.

- [Иконнектионпоинтконтаинеримпл](../atl/reference/iconnectionpointcontainerimpl-class.md) реализует контейнер точки подключения и управляет списком `IConnectionPointImpl` объектов.

- [Ипропертинотифисинккп](../atl/reference/ipropertynotifysinkcp-class.md) реализует точку соединения, представляющую интерфейс [ипропертинотифисинк](/windows/win32/api/ocidl/nn-ocidl-ipropertynotifysink) .

- [Ккомдинамикункаррай](../atl/reference/ccomdynamicunkarray-class.md) управляет произвольным числом соединений между точкой подключения и ее приемниками.

- [Ккомункаррай](../atl/reference/ccomunkarray-class.md) управляет стандартным количеством соединений, указанным параметром шаблона.

- [Кфирепропнотифевент](../atl/reference/cfirepropnotifyevent-class.md) уведомляет приемник клиента, что свойство объекта изменилось или собирается его изменить.

- [IDispEventImpl](../atl/reference/idispeventimpl-class.md) обеспечивает поддержку точек соединения для COM-объекта ATL. Эти точки соединения сопоставляются с картой приемника событий, которая предоставляется объектом COM.

- [IDispEventSimpleImpl](../atl/reference/idispeventsimpleimpl-class.md) работает в сочетании с картой приемника событий в классе для маршрутизации событий в соответствующую функцию обработчика.

## <a name="see-also"></a>См. также раздел

[Точка подключения](../atl/atl-connection-points.md)
