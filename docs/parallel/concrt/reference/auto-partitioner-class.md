---
description: 'Дополнительные сведения о: auto_partitioner классе'
title: Класс auto_partitioner
ms.date: 11/04/2016
f1_keywords:
- auto_partitioner
- PPL/concurrency::auto_partitioner
- PPL/concurrency::auto_partitioner::auto_partitioner
helpviewer_keywords:
- auto_partitioner class
ms.assetid: 7cc08e5d-20b4-47a4-b4b5-c214a78f5a9e
ms.openlocfilehash: d8e099c7a3132ce89f81df65d7e18a5c6c673697
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97172262"
---
# <a name="auto_partitioner-class"></a>Класс auto_partitioner

Класс `auto_partitioner` представляет метод, который алгоритмы `parallel_for`, `parallel_for_each` и `parallel_transform` используют по умолчанию для разделения обрабатываемого диапазона. Этот метод секционирования использует перенос диапазона для балансировки нагрузки, а также для отмены при переборе.

## <a name="syntax"></a>Синтаксис

```cpp
class auto_partitioner;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[auto_partitioner](#ctor)|Формирует объект `auto_partitioner`.|
|[Деструктор ~ auto_partitioner](#dtor)|Уничтожает объект `auto_partitioner` .|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`auto_partitioner`

## <a name="requirements"></a>Требования

**Заголовок:** PPL. h

**Пространство имен:** параллелизм

## <a name="auto_partitioner"></a><a name="dtor"></a> ~ auto_partitioner

Уничтожает объект `auto_partitioner` .

```cpp
~auto_partitioner();
```

## <a name="auto_partitioner"></a><a name="ctor"></a> auto_partitioner

Формирует объект `auto_partitioner`.

```cpp
auto_partitioner();
```

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency](concurrency-namespace.md)
