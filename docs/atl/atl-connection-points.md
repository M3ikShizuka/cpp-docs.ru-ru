---
description: Дополнительные сведения см. в статье точки подключения ATL.
title: Точки подключения ATL
ms.date: 11/04/2016
helpviewer_keywords:
- connections, connection points
- ATL, connection points
- connection points [C++], about connection points
ms.assetid: 17d76165-5f83-4f95-b36d-483821c247a1
ms.openlocfilehash: 60b9018185bea2af26407ee9d7a203148c8dc477
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97165827"
---
# <a name="atl-connection-points"></a>Точки подключения ATL

Доступный для подключения объект поддерживает исходящие интерфейсы. Исходящий интерфейс позволяет объекту обмениваться данными с клиентом. Для каждого исходящего интерфейса доступный для подключения объект предоставляет точку подключения. Каждый исходящий интерфейс реализуется клиентов для объекта, который называется приемником.

![Точки подключения](../atl/media/vc2zw31.gif "Точки подключения")

Каждая точка подключения поддерживает интерфейс [IConnectionPoint](/windows/win32/api/ocidl/nn-ocidl-iconnectionpoint) . Подключаемый объект предоставляет клиенту точки подключения через интерфейс [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) .

## <a name="in-this-section"></a>в этом разделе

[Классы точек подключения ATL](../atl/atl-connection-point-classes.md)<br/>
Краткое описание классов ATL, поддерживающих точки подключения.

[Добавление точек подключения к объекту](../atl/adding-connection-points-to-an-object.md)<br/>
Описываются действия для добавления точек подключения к объекту.

[Пример точки подключения ATL](../atl/atl-connection-point-example.md)<br/>
Пример объявления точки подключения.

## <a name="related-sections"></a>Связанные разделы

[ATL](../atl/active-template-library-atl-concepts.md)<br/>
Ссылки на разделы о программировании с использованием библиотеки ATL.

## <a name="see-also"></a>См. также раздел

[Основные понятия](../atl/active-template-library-atl-concepts.md)
