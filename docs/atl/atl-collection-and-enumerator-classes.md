---
description: 'Дополнительные сведения: классы коллекций и перечислителей ATL'
title: Классы коллекций и перечислителей ATL
ms.date: 11/04/2016
helpviewer_keywords:
- enumerators, ATL classes
- collection classes, ATL
ms.assetid: 6818db73-7094-48d8-a0ca-18147beec362
ms.openlocfilehash: b1f30aabb4908b0299a927f92a6d5ee4e9370a09
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97166048"
---
# <a name="atl-collection-and-enumerator-classes"></a>Классы коллекций и перечислителей ATL

ATL предоставляет следующие классы, помогающие реализовать коллекции и перечислители.

|Класс|Описание|
|-----------|-----------------|
|[иколлектиононстлимпл](../atl/reference/icollectiononstlimpl-class.md)|Реализация интерфейса коллекции|
|[иенумонстлимпл](../atl/reference/ienumonstlimpl-class.md)|Реализация интерфейса перечислителя (предполагается, что данные хранятся в контейнере, совместимом с стандартной библиотекой C++)|
|[ккоменумимпл](../atl/reference/ccomenumimpl-class.md)|Реализация интерфейса перечислителя (предполагается, что данные хранятся в массиве)|
|[ккоменумонстл](../atl/reference/ccomenumonstl-class.md)|Реализация объекта Enumerator (использует `IEnumOnSTLImpl` )|
|[ккоменум](../atl/reference/ccomenum-class.md)|Реализация объекта Enumerator (использует `CComEnumImpl` )|
|[_Copy](../atl/atl-copy-policy-classes.md)|Копирование класса политики|
|[_CopyInterface](../atl/atl-copy-policy-classes.md)|Копирование класса политики|
|[кадапт](../atl/reference/cadapt-class.md)|Класс адаптера (скрывает **оператор, &** позволяющий `CComPtr` `CComQIPtr` сохранять, и `CComBSTR` хранить в контейнерах стандартной библиотеки C++)|

## <a name="see-also"></a>См. также раздел

[Коллекции и перечислители](../atl/atl-collections-and-enumerators.md)
