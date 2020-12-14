---
description: 'Дополнительные сведения: структура scheduler_interface'
title: Структура scheduler_interface
ms.date: 11/04/2016
f1_keywords:
- scheduler_interface
- PPLINTERFACE/concurrency::scheduler_interface
- PPLINTERFACE/concurrency::scheduler_interface::scheduler_interface::schedule
ms.assetid: 4de61c78-a2c6-4698-bd47-964baf7fa287
ms.openlocfilehash: ba56ef809cf398a192810eb96a8b4e4ca50ec1cc
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97188876"
---
# <a name="scheduler_interface-structure"></a>Структура scheduler_interface

Интерфейс планировщика

## <a name="syntax"></a>Синтаксис

```cpp
struct __declspec(novtable) scheduler_interface;
```

## <a name="members"></a>Члены

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[scheduler_interface:: Schedule](#schedule)||

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`scheduler_interface`

## <a name="requirements"></a>Требования

**Заголовок:** пплинтерфаце. h

**Пространство имен:** параллелизм

## <a name="scheduler_interfaceschedule-method"></a><a name="schedule"></a> Метод scheduler_interface:: Schedule

```cpp
virtual void schedule(
    TaskProc_t,
void*) = 0;
```

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency](concurrency-namespace.md)
