---
description: 'Дополнительные сведения: изменение фабрики классов по умолчанию и статистической модели'
title: Изменение фабрики классов по умолчанию и статистической модели
ms.date: 11/04/2016
helpviewer_keywords:
- CComClassFactory class, making the default
- aggregation [C++], using ATL
- aggregation [C++], aggregation models
- defaults [C++], aggregation model in ATL
- default class factory
- class factories, changing default
- CComCoClass class, default class factory and aggregation model
- default class factory, ATL
- defaults [C++], class factory
ms.assetid: 6e040e95-0f38-4839-8a8b-c9800dd47e8c
ms.openlocfilehash: b25dc1c2cf3378532f02b1c0d5ba56cd43ee4ae4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97148282"
---
# <a name="changing-the-default-class-factory-and-aggregation-model"></a>Изменение фабрики классов по умолчанию и статистической модели

ATL использует [CComCoClass](../atl/reference/ccomcoclass-class.md) для определения фабрики класса по умолчанию и статистической модели для объекта. `CComCoClass` задает следующие два макроса:

- [DECLARE_CLASSFACTORY](reference/aggregation-and-class-factory-macros.md#declare_classfactory) Объявляет фабрику класса для [ккомклассфактори](../atl/reference/ccomclassfactory-class.md).

- [DECLARE_AGGREGATABLE](reference/aggregation-and-class-factory-macros.md#declare_aggregatable) Объявляет, что объект может быть агрегирован.

Можно переопределить любое из этих значений по умолчанию, указав другой макрос в определении класса. Например, чтобы использовать [CComClassFactory2](../atl/reference/ccomclassfactory2-class.md) вместо `CComClassFactory` , укажите макрос [DECLARE_CLASSFACTORY2](reference/aggregation-and-class-factory-macros.md#declare_classfactory2) :

[!code-cpp[NVC_ATL_COM#2](../atl/codesnippet/cpp/changing-the-default-class-factory-and-aggregation-model_1.h)]

Два других макроса, определяющих фабрику класса, [DECLARE_CLASSFACTORY_AUTO_THREAD](reference/aggregation-and-class-factory-macros.md#declare_classfactory_auto_thread) и [DECLARE_CLASSFACTORY_SINGLETON](reference/aggregation-and-class-factory-macros.md#declare_classfactory_singleton).

ATL также использует **`typedef`** механизм для реализации поведения по умолчанию. Например, DECLARE_AGGREGATABLE макрос использует **`typedef`** для определения типа с именем `_CreatorClass` , который затем упоминается в библиотеке ATL. Обратите внимание, что в производном классе, **`typedef`** используя то же имя, что и базовый класс, **`typedef`** в библиотеке ATL с помощью определения и переопределения поведения по умолчанию.

## <a name="see-also"></a>См. также раздел

[Основы COM-объектов ATL](../atl/fundamentals-of-atl-com-objects.md)<br/>
[Макросы агрегирования и фабрики классов](../atl/reference/aggregation-and-class-factory-macros.md)
