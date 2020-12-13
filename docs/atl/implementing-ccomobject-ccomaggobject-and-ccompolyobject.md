---
description: 'Дополнительные сведения: реализация CComObject, CComAggObject и CComPolyObject'
title: Реализация CComObject, CComAggObject и CComPolyObject
ms.date: 11/04/2016
helpviewer_keywords:
- CComPolyObject class, implementing
- CreateInstance method
- CComAggObject class
- CComObject class, implementing
ms.assetid: 5aabe938-104d-492e-9c41-9f7fb1c62098
ms.openlocfilehash: e0cc8a6b65ec9d85249cd47e2f43cf1bec2b8ce2
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97147775"
---
# <a name="implementing-ccomobject-ccomaggobject-and-ccompolyobject"></a>Реализация CComObject, CComAggObject и CComPolyObject

Классы шаблонов [CComObject](../atl/reference/ccomobject-class.md), [CComAggObject](../atl/reference/ccomaggobject-class.md)и [CComPolyObject](../atl/reference/ccompolyobject-class.md) всегда являются самыми производными классами в цепочке наследования. Ответственность за обработку всех методов в `IUnknown` : `QueryInterface` , `AddRef` и `Release` . Кроме того, `CComAggObject` и `CComPolyObject` (при использовании для агрегированных объектов) предоставляют специальный подсчет ссылок и `QueryInterface` семантику, необходимую для внутреннего неизвестного.

`CComObject`Используется ли, `CComAggObject` или, зависит от того, `CComPolyObject` объявлены ли вы (или нет) следующих макросов:

|Макрос|Действие|
|-----------|------------|
|DECLARE_NOT_AGGREGATABLE|Всегда использует `CComObject` .|
|DECLARE_AGGREGATABLE|Использует, `CComAggObject` Если объект является агрегатным и `CComObject` Если нет. `CComCoClass` содержит этот макрос, поэтому, если в классе не объявлен ни один из макросов DECLARE_ * _AGGREGATABLE, это будет значение по умолчанию.|
|DECLARE_ONLY_AGGREGATABLE|Всегда использует `CComAggObject` . Возвращает ошибку, если объект не является агрегированным.|
|DECLARE_POLY_AGGREGATABLE|При вызове библиотеки ATL создает экземпляр **CComPolyObject \<CYourClass>** `IClassFactory::CreateInstance` . Во время создания проверяется значение внешней неизвестной. Если он равен NULL, `IUnknown` реализуется для неагрегированного объекта. Если внешнее неизвестное значение не равно NULL, `IUnknown` реализуется для агрегированного объекта.|

Преимуществом использования `CComAggObject` и является то `CComObject` , что реализация `IUnknown` оптимизирована для вида создаваемого объекта. Например, неагрегированный объект требует только счетчика ссылок, в то время как для агрегированного объекта требуется как счетчик ссылок для внутреннего элемента Unknown, так и указатель на внешнее неизвестное значение.

Преимущество использования заключается в том `CComPolyObject` , что не следует одновременно использовать `CComAggObject` и `CComObject` в модуле для обработки агрегированных и неагрегированных вариантов. В `CComPolyObject` обоих случаях обрабатывается один объект. Это означает, что в модуле существует только одна копия таблицы vtable и одна копия функций. Если таблица vtable велика, это может значительно снизить размер модуля. Однако если таблица vtable невелика, использование `CComPolyObject` может привести к тому, что размер модуля будет немного больше, поскольку он не оптимизирован для агрегированного или неагрегированного объекта, как `CComAggObject` и `CComObject` .

## <a name="see-also"></a>См. также раздел

[Основы COM-объектов ATL](../atl/fundamentals-of-atl-com-objects.md)<br/>
[Макросы агрегирования и фабрики классов](../atl/reference/aggregation-and-class-factory-macros.md)
