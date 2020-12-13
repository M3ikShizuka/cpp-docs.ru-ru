---
description: 'Дополнительные сведения о: структура ITopologyExecutionResource'
title: Структура ITopologyExecutionResource
ms.date: 11/04/2016
f1_keywords:
- ITopologyExecutionResource
- CONCRTRM/concurrency::ITopologyExecutionResource
- CONCRTRM/concurrency::ITopologyExecutionResource::ITopologyExecutionResource::GetId
- CONCRTRM/concurrency::ITopologyExecutionResource::ITopologyExecutionResource::GetNext
helpviewer_keywords:
- ITopologyExecutionResource structure
ms.assetid: e36756f7-4cd9-4fa6-ba60-23fea58ef2bf
ms.openlocfilehash: c2567cf9e34e0b27308e331056d5e0dbc99b2779
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97334383"
---
# <a name="itopologyexecutionresource-structure"></a>Структура ITopologyExecutionResource

Интерфейс для ресурса выполнения, как определено диспетчером ресурсов.

## <a name="syntax"></a>Синтаксис

```cpp
struct ITopologyExecutionResource;
```

## <a name="members"></a>Члены

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[ITopologyExecutionResource:: GetId](#getid)|Возвращает уникальный идентификатор диспетчера ресурсов для данного ресурса выполнения.|
|[ITopologyExecutionResource:: GetNext](#getnext)|Возвращает интерфейс для следующего ресурса выполнения в порядке перечисления.|

## <a name="remarks"></a>Комментарии

Этот интерфейс обычно используется для анализа топологии системы, наблюдаемой диспетчер ресурсов.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`ITopologyExecutionResource`

## <a name="requirements"></a>Требования

**Заголовок:** concrtrm. h

**Пространство имен:** параллелизм

## <a name="itopologyexecutionresourcegetid-method"></a><a name="getid"></a> Метод ITopologyExecutionResource:: GetId

Возвращает уникальный идентификатор диспетчера ресурсов для данного ресурса выполнения.

```cpp
virtual unsigned int GetId() const = 0;
```

### <a name="return-value"></a>Возвращаемое значение

Уникальный идентификатор диспетчера ресурсов для данного ресурса выполнения.

## <a name="itopologyexecutionresourcegetnext-method"></a><a name="getnext"></a> Метод ITopologyExecutionResource:: GetNext

Возвращает интерфейс для следующего ресурса выполнения в порядке перечисления.

```cpp
virtual ITopologyExecutionResource *GetNext() const = 0;
```

### <a name="return-value"></a>Возвращаемое значение

Интерфейс для следующего ресурса выполнения в порядке перечисления. Если больше нет узлов в порядке перечисления узла, которому принадлежит этот ресурс выполнения, этот метод возвращает значение `NULL`.

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency](concurrency-namespace.md)
