---
description: Дополнительные сведения см. в статье реализация интерфейса обработки событий.
title: Реализация интерфейса обработки событий
ms.date: 11/04/2016
helpviewer_keywords:
- ATL, event handling
- event handling, ATL
- interfaces, event and event sink
ms.assetid: eb2a5b33-88dc-4ce3-bee0-c5c38ea050d7
ms.openlocfilehash: 109fbb1fbdd4f18d0eb4c295fbc08de2b7cc3a35
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97152767"
---
# <a name="implementing-the-event-handling-interface"></a>Реализация интерфейса обработки событий

ATL помогает выполнить все три элемента, необходимые для обработки событий: реализация интерфейса событий, предоставление источника событий и отключение источника событий. Точные действия, которые необходимо выполнить, зависят от типа интерфейса событий и требований к производительности приложения.

Ниже перечислены наиболее распространенные способы реализации интерфейса с помощью ATL.

- Наследование от пользовательского интерфейса напрямую.

- Наследование от [IDispatchImpl](../atl/reference/idispatchimpl-class.md) для сдвоенных интерфейсов, описанных в библиотеке типов.

- Наследование от [IDispEventImpl](../atl/reference/idispeventimpl-class.md) для disp-интерфейсов, описанных в библиотеке типов.

- Наследование от [IDispEventSimpleImpl](../atl/reference/idispeventsimpleimpl-class.md) для disp-интерфейсов, не описанных в библиотеке типов, или если требуется повысить эффективность, не загружая сведения о типе во время выполнения.

При реализации пользовательского или сдвоенного интерфейса следует рекомендовать источник события, вызвав [атладвисе](reference/connection-point-global-functions.md#atladvise) или [Ккомптрбасе:: Advise](../atl/reference/ccomptrbase-class.md#advise). Необходимо будет отследить файл cookie, возвращенный вызовом самостоятельно. Вызовите [атлунадвисе](reference/connection-point-global-functions.md#atlunadvise) , чтобы разорвать соединение.

При реализации disp-интерфейса с помощью `IDispEventImpl` или `IDispEventSimpleImpl` следует рекомендовать источник события, вызвав [IDispEventSimpleImpl::D испевентадвисе](../atl/reference/idispeventsimpleimpl-class.md#dispeventadvise). Вызовите [IDispEventSimpleImpl::D испевентунадвисе](../atl/reference/idispeventsimpleimpl-class.md#dispeventunadvise) , чтобы разорвать соединение.

Если вы используете в `IDispEventImpl` качестве базового класса составного элемента управления, то источники событий, перечисленные в схеме приемника, будут рекомендоваться и не были бы автоматически использоваться с помощью [ккомкомпоситеконтрол:: адвисесинкмап](../atl/reference/ccomcompositecontrol-class.md#advisesinkmap).

`IDispEventImpl`Классы и `IDispEventSimpleImpl` управляют этим файлом cookie.

## <a name="see-also"></a>См. также раздел

[Обработка событий](../atl/event-handling-and-atl.md)
