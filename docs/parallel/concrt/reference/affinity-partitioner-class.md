---
description: 'Дополнительные сведения о: affinity_partitioner классе'
title: Класс affinity_partitioner
ms.date: 11/04/2016
f1_keywords:
- affinity_partitioner
- PPL/concurrency::affinity_partitioner
- PPL/concurrency::affinity_partitioner::affinity_partitioner
helpviewer_keywords:
- affinity_partitioner class
ms.assetid: 31bf7bb1-bd01-491c-9760-d9d60edfccad
ms.openlocfilehash: 44aa693d5007507e33f062a673713d1ddbda3172
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97172327"
---
# <a name="affinity_partitioner-class"></a>Класс affinity_partitioner

Класс `affinity_partitioner` аналогичен классу `static_partitioner`, но он повышает сходство кэша путем подбора поддиапазонов сопоставления для потоков рабочего процесса. Он может значительно повысить производительность, если цикл повторно выполняется в одном и том же наборе данных и данные помещаются в кэш. Обратите внимание, что один и тот же объект `affinity_partitioner` должен использоваться с последующими итерациями параллельного цикла, выполняемого в указанном наборе данных, чтобы воспользоваться преимуществом локальности данных.

## <a name="syntax"></a>Синтаксис

```cpp
class affinity_partitioner;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[affinity_partitioner](#ctor)|Создает объект `affinity_partitioner`.|
|[Деструктор ~ affinity_partitioner](#dtor)|Уничтожает `affinity_partitioner` объект.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`affinity_partitioner`

## <a name="requirements"></a>Требования

**Заголовок:** PPL. h

**Пространство имен:** параллелизм

## <a name="affinity_partitioner"></a><a name="dtor"></a> ~ affinity_partitioner

Уничтожает `affinity_partitioner` объект.

```cpp
~affinity_partitioner();
```

## <a name="affinity_partitioner"></a><a name="ctor"></a> affinity_partitioner

Создает объект `affinity_partitioner`.

```cpp
affinity_partitioner();
```

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency](concurrency-namespace.md)
