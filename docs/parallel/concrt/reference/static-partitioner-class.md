---
description: 'Дополнительные сведения о: static_partitioner классе'
title: Класс static_partitioner
ms.date: 11/04/2016
f1_keywords:
- static_partitioner
- PPL/concurrency::static_partitioner
- PPL/concurrency::static_partitioner::static_partitioner
helpviewer_keywords:
- static_partitioner class
ms.assetid: 2b3dbdf0-6eb9-49f6-8639-03df1d974143
ms.openlocfilehash: f75d2e620a66e0ed347d39d429f59e3e2715369a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97188499"
---
# <a name="static_partitioner-class"></a>Класс static_partitioner

Класс `static_partitioner` представляет статическое разделение диапазона, в котором итерации выполняются с помощью `parallel_for`. Модуль разделения разделяет диапазон на количество фрагментов, доступных для базового планировщика.

## <a name="syntax"></a>Синтаксис

```cpp
class static_partitioner;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[static_partitioner](#ctor)|Формирует объект `static_partitioner`.|
|[Деструктор ~ static_partitioner](#dtor)|Уничтожает объект `static_partitioner` .|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`static_partitioner`

## <a name="requirements"></a>Требования

**Заголовок:** PPL. h

**Пространство имен:** параллелизм

## <a name="static_partitioner"></a><a name="dtor"></a> ~ static_partitioner

Уничтожает объект `static_partitioner` .

```cpp
~static_partitioner();
```

## <a name="static_partitioner"></a><a name="ctor"></a> static_partitioner

Формирует объект `static_partitioner`.

```cpp
static_partitioner();
```

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency](concurrency-namespace.md)
