---
description: 'Дополнительные сведения о: структура IExecutionContext'
title: Структура IExecutionContext
ms.date: 11/04/2016
f1_keywords:
- IExecutionContext
- CONCRTRM/concurrency::IExecutionContext
- CONCRTRM/concurrency::IExecutionContext::IExecutionContext::Dispatch
- CONCRTRM/concurrency::IExecutionContext::IExecutionContext::GetId
- CONCRTRM/concurrency::IExecutionContext::IExecutionContext::GetProxy
- CONCRTRM/concurrency::IExecutionContext::IExecutionContext::GetScheduler
- CONCRTRM/concurrency::IExecutionContext::IExecutionContext::SetProxy
helpviewer_keywords:
- IExecutionContext structure
ms.assetid: f3108089-ecda-4b07-86db-3efae60c31e0
ms.openlocfilehash: 90802229e878546383f683bc99ffedc9cb5411af
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97122191"
---
# <a name="iexecutioncontext-structure"></a>Структура IExecutionContext

Интерфейс для контекста выполнения, который может выполняться на данном виртуальном процессоре и к которому может применяться совместное переключение контекста.

## <a name="syntax"></a>Синтаксис

```cpp
struct IExecutionContext;
```

## <a name="members"></a>Члены

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[IExecutionContext::D Patch](#dispatch)|Метод, вызываемый, когда прокси-поток запускает выполнение определенного контекста выполнения. Это должна быть Основная рабочая подпрограммы для планировщика.|
|[IExecutionContext:: GetId](#getid)|Возвращает уникальный идентификатор контекста выполнения.|
|[IExecutionContext::-proxy](#getproxy)|Возвращает интерфейс прокси-сервера потока, который исполняет этот контекст.|
|[IExecutionContext:: "Scheduler"](#getscheduler)|Возвращает интерфейс к планировщику, которому принадлежит контекст выполнения.|
|[IExecutionContext:: Сетпрокси](#setproxy)|Связывает прокси-поток с этим контекстом выполнения. Связанный прокси-поток вызывает этот метод прямо перед выполнением `Dispatch` метода контекста.|

## <a name="remarks"></a>Комментарии

При реализации пользовательского планировщика, который взаимодействует с диспетчер ресурсовом среда выполнения с параллелизмом, необходимо реализовать `IExecutionContext` интерфейс. Потоки, созданные диспетчер ресурсов, выполняют работу от имени планировщика, выполняя `IExecutionContext::Dispatch` метод.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`IExecutionContext`

## <a name="requirements"></a>Требования

**Заголовок:** concrtrm. h

**Пространство имен:** параллелизм

## <a name="iexecutioncontextdispatch-method"></a><a name="dispatch"></a> IExecutionContext::D метода Patch

Метод, вызываемый, когда прокси-поток запускает выполнение определенного контекста выполнения. Это должна быть Основная рабочая подпрограммы для планировщика.

```cpp
virtual void Dispatch(_Inout_ DispatchState* pDispatchState) = 0;
```

### <a name="parameters"></a>Параметры

*пдиспатчстате*<br/>
Указатель на состояние, под которым отправляется этот контекст выполнения. Дополнительные сведения о состоянии диспетчеризации см. в разделе [DispatchState](dispatchstate-structure.md).

## <a name="iexecutioncontextgetid-method"></a><a name="getid"></a> Метод IExecutionContext:: GetId

Возвращает уникальный идентификатор контекста выполнения.

```cpp
virtual unsigned int GetId() const = 0;
```

### <a name="return-value"></a>Возвращаемое значение

Уникальный целочисленный идентификатор.

### <a name="remarks"></a>Комментарии

Метод следует использовать `GetExecutionContextId` для получения уникального идентификатора объекта, реализующего `IExecutionContext` интерфейс, перед использованием интерфейса в качестве параметра для методов, предоставляемых диспетчер ресурсов. При вызове функции ожидается возврат одного и того же идентификатора `GetId` .

Идентификатор, полученный из другого источника, может привести к неопределенному поведению.

## <a name="iexecutioncontextgetproxy-method"></a><a name="getproxy"></a> Метод IExecutionContext::-proxy

Возвращает интерфейс прокси-сервера потока, который исполняет этот контекст.

```cpp
virtual IThreadProxy* GetProxy() = 0;
```

### <a name="return-value"></a>Возвращаемое значение

Интерфейс `IThreadProxy`. Если прокси-сервер потока контекста выполнения не был инициализирован с помощью вызова `SetProxy` функции, функция должна возвращать значение `NULL` .

### <a name="remarks"></a>Комментарии

Диспетчер ресурсов вызовет `SetProxy` метод для контекста выполнения с `IThreadProxy` интерфейсом в качестве параметра перед входом в `Dispatch` метод в контексте. Вы должны сохранить этот аргумент и вернуть его при вызовах `GetProxy()` .

## <a name="iexecutioncontextgetscheduler-method"></a><a name="getscheduler"></a> Метод IExecutionContext:: Scheduler

Возвращает интерфейс к планировщику, которому принадлежит контекст выполнения.

```cpp
virtual IScheduler* GetScheduler() = 0;
```

### <a name="return-value"></a>Возвращаемое значение

Интерфейс `IScheduler`.

### <a name="remarks"></a>Комментарии

Необходимо инициализировать контекст выполнения с допустимым `IScheduler` интерфейсом, прежде чем использовать его в качестве параметра для методов, предоставляемых диспетчер ресурсов.

## <a name="iexecutioncontextsetproxy-method"></a><a name="setproxy"></a> Метод IExecutionContext:: Сетпрокси

Связывает прокси-поток с этим контекстом выполнения. Связанный прокси-поток вызывает этот метод прямо перед выполнением `Dispatch` метода контекста.

```cpp
virtual void SetProxy(_Inout_ IThreadProxy* pThreadProxy) = 0;
```

### <a name="parameters"></a>Параметры

*псреадпрокси*<br/>
Интерфейс для прокси-сервера потока, который собирается ввести `Dispatch` метод в данном контексте выполнения.

### <a name="remarks"></a>Комментарии

Предполагается, что параметр будет сохранен `pThreadProxy` и возвращен при вызове `GetProxy` метода. Диспетчер ресурсов гарантирует, что прокси-сервер потока, связанный с контекстом выполнения, не изменится во время выполнения метода прокси-потоком `Dispatch` .

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency](concurrency-namespace.md)<br/>
[Структура IScheduler](ischeduler-structure.md)<br/>
[Структура IThreadProxy](ithreadproxy-structure.md)
