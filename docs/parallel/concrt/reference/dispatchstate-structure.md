---
description: 'Дополнительные сведения о: структура DispatchState'
title: Структура DispatchState
ms.date: 11/04/2016
f1_keywords:
- DispatchState
- CONCRTRM/concurrency::DispatchState
- CONCRTRM/concurrency::DispatchState::DispatchState::DispatchState
- CONCRTRM/concurrency::DispatchState::DispatchState::m_dispatchStateSize
- CONCRTRM/concurrency::DispatchState::DispatchState::m_fIsPreviousContextAsynchronouslyBlocked
- CONCRTRM/concurrency::DispatchState::DispatchState::m_reserved
helpviewer_keywords:
- DispatchState structure
ms.assetid: 8c52546e-1650-48a0-985f-7e4a0fc26a90
ms.openlocfilehash: 1352a283d6f75d90872e75da92450a4867cf497f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97169428"
---
# <a name="dispatchstate-structure"></a>Структура DispatchState

Структура `DispatchState` используется для передачи состояния в метод `IExecutionContext::Dispatch`. Она описывает обстоятельства, при которых метод `Dispatch` вызывается для интерфейса `IExecutionContext`.

## <a name="syntax"></a>Синтаксис

```cpp
struct DispatchState;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[DispatchState::D Испатчстате](#ctor)|Создает новый объект `DispatchState`.|

### <a name="public-data-members"></a>Открытые члены данных

|Имя|Описание|
|----------|-----------------|
|[DispatchState:: m_dispatchStateSize](#m_dispatchstatesize)|Размер этой структуры, которая используется для управления версиями.|
|[DispatchState:: m_fIsPreviousContextAsynchronouslyBlocked](#m_fispreviouscontextasynchronouslyblocked)|Сообщает, вошел ли этот метод в этот контекст из- `Dispatch` за асинхронной блокировки предыдущего контекста. Он используется только в контексте планирования UMS и устанавливается в значение `0` для всех других контекстов выполнения.|
|[DispatchState:: m_reserved](#m_reserved)|Биты, зарезервированные для будущей передачи информации.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`DispatchState`

## <a name="requirements"></a>Требования

**Заголовок:** concrtrm. h

**Пространство имен:** параллелизм

## <a name="dispatchstatedispatchstate-constructor"></a><a name="ctor"></a> DispatchState: конструктор:D Испатчстате

Создает новый объект `DispatchState`.

```cpp
DispatchState();
```

## <a name="dispatchstatem_dispatchstatesize-data-member"></a><a name="m_dispatchstatesize"></a> Элемент данных DispatchState:: m_dispatchStateSize

Размер этой структуры, которая используется для управления версиями.

```cpp
unsigned long m_dispatchStateSize;
```

## <a name="dispatchstatem_fispreviouscontextasynchronouslyblocked-data-member"></a><a name="m_fispreviouscontextasynchronouslyblocked"></a> Элемент данных DispatchState:: m_fIsPreviousContextAsynchronouslyBlocked

Сообщает, вошел ли этот метод в этот контекст из- `Dispatch` за асинхронной блокировки предыдущего контекста. Он используется только в контексте планирования UMS и устанавливается в значение `0` для всех других контекстов выполнения.

```cpp
unsigned int m_fIsPreviousContextAsynchronouslyBlocked : 1;
```

## <a name="dispatchstatem_reserved-data-member"></a><a name="m_reserved"></a> Элемент данных DispatchState:: m_reserved

Биты, зарезервированные для будущей передачи информации.

```cpp
unsigned int m_reserved : 31;
```

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency](concurrency-namespace.md)
