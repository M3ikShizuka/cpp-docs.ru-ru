---
description: 'Дополнительные сведения: классы реализации IUnknown'
title: Классы реализации IUnknown (ATL)
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IUnknown implementation classes
ms.assetid: 47b69bb5-69d8-4a9c-84a8-329bdde2bb3f
ms.openlocfilehash: a28bd14be86501fd6566b8038b73a51efcc1c18d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97147658"
---
# <a name="iunknown-implementation-classes"></a>Классы реализации IUnknown

Следующие классы реализуют `IUnknown` и взаимосвязанные методы:

- [CComObjectRootEx](../atl/reference/ccomobjectrootex-class.md) Управляет подсчетом ссылок как для агрегированных, так и для неагрегированных объектов. Позволяет указать потоковую модель.

- [CComObjectRoot](../atl/reference/ccomobjectroot-class.md) Управляет подсчетом ссылок как для агрегированных, так и для неагрегированных объектов. Использует модель потоков по умолчанию сервера.

- [CComAggObject](../atl/reference/ccomaggobject-class.md) Реализует `IUnknown` для агрегированного объекта.

- [CComObject](../atl/reference/ccomobject-class.md) Реализует `IUnknown` для неагрегированного объекта.

- [CComPolyObject](../atl/reference/ccompolyobject-class.md) Реализует `IUnknown` для агрегированных и неагрегированных объектов. `CComPolyObject`При использовании не следует использовать `CComAggObject` и `CComObject` в модуле. Один `CComPolyObject` объект обрабатывает как агрегированные, так и неагрегированные варианты.

- [Ккомобжектнолокк](../atl/reference/ccomobjectnolock-class.md) Реализует `IUnknown` для неагрегированного объекта без изменения счетчика блокировок модуля.

- [Ккомтеароффобжект](../atl/reference/ccomtearoffobject-class.md) Реализует `IUnknown` интерфейс для разрыва.

- [Ккомкачедтеароффобжект](../atl/reference/ccomcachedtearoffobject-class.md) Реализует `IUnknown` для "кэшированного" интерфейса разрыва.

- [Ккомконтаинедобжект](../atl/reference/ccomcontainedobject-class.md) Реализует `IUnknown` для внутреннего объекта агрегата или интерфейса разрыва.

- [Ккомобжектглобал](../atl/reference/ccomobjectglobal-class.md) Управляет счетчиком ссылок на модуль, чтобы объект не был удален.

- [Ккомобжектстакк](../atl/reference/ccomobjectstack-class.md) Создает временный COM-объект с помощью реализации скелетообразных `IUnknown` .

## <a name="related-articles"></a>Похожие статьи

[Основы COM-объектов ATL](../atl/fundamentals-of-atl-com-objects.md)

## <a name="see-also"></a>См. также раздел

[Общие сведения о классах](../atl/atl-class-overview.md)<br/>
[Макросы агрегирования и фабрики классов](../atl/reference/aggregation-and-class-factory-macros.md)<br/>
[Макросы схемы COM](../atl/reference/com-map-macros.md)<br/>
[Глобальные функции схемы COM](../atl/reference/com-map-global-functions.md)
