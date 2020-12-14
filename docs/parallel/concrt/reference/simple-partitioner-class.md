---
description: 'Дополнительные сведения о: simple_partitioner классе'
title: Класс simple_partitioner
ms.date: 11/04/2016
f1_keywords:
- simple_partitioner
- PPL/concurrency::simple_partitioner
- PPL/concurrency::simple_partitioner::simple_partitioner
helpviewer_keywords:
- simple_partitioner class
ms.assetid: d7e997af-54d1-43f5-abe0-def72df6edb3
ms.openlocfilehash: 76dcac6d7fc2dce5b69d0a9dbefaf01420f8bcde
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97188694"
---
# <a name="simple_partitioner-class"></a>Класс simple_partitioner

Класс `simple_partitioner` представляет статическое разделение диапазона, в котором итерации выполняются с помощью `parallel_for`. Разделитель делит диапазон на фрагменты таким образом, что каждый фрагмент имеет число итераций не менее указанного размера фрагмента.

## <a name="syntax"></a>Синтаксис

```cpp
class simple_partitioner;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[simple_partitioner](#ctor)|Формирует объект `simple_partitioner`.|
|[Деструктор ~ simple_partitioner](#dtor)|Уничтожает объект `simple_partitioner` .|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`simple_partitioner`

## <a name="requirements"></a>Требования

**Заголовок:** PPL. h

**Пространство имен:** параллелизм

## <a name="simple_partitioner"></a><a name="dtor"></a> ~ simple_partitioner

Уничтожает объект `simple_partitioner` .

```cpp
~simple_partitioner();
```

## <a name="simple_partitioner"></a><a name="ctor"></a> simple_partitioner

Формирует объект `simple_partitioner`.

```cpp
explicit simple_partitioner(_Size_type _Chunk_size);
```

### <a name="parameters"></a>Параметры

*_Chunk_size*<br/>
Минимальный размер раздела.

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency](concurrency-namespace.md)
