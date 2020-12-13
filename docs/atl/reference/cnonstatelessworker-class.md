---
description: 'Дополнительные сведения о: Кнонстателессворкер Class'
title: Класс Кнонстателессворкер
ms.date: 11/04/2016
f1_keywords:
- CNonStatelessWorker
- ATLUTIL/ATL::CNonStatelessWorker
- ATLUTIL/ATL::CNonStatelessWorker::RequestType
- ATLUTIL/ATL::CNonStatelessWorker::Execute
- ATLUTIL/ATL::CNonStatelessWorker::Initialize
- ATLUTIL/ATL::CNonStatelessWorker::Terminate
helpviewer_keywords:
- CNonStatelessWorker class
ms.assetid: d00936c6-9e7d-49fb-b87d-417b963367d1
ms.openlocfilehash: 68457c9594bfaf4d8dd53acd80d7997355c3a3f5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97141431"
---
# <a name="cnonstatelessworker-class"></a>Класс Кнонстателессворкер

Получает запросы из пула потоков и передает их в рабочий объект, который создается и уничтожается при каждом запросе.

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```
template <class Worker>
class CNonStatelessWorker
```

#### <a name="parameters"></a>Параметры

*Рабочий узел*<br/>
Класс рабочего потока, соответствующий [рабочему](../../atl/reference/worker-archetype.md) потоку архетипа, подходящему для обработки запросов, поставленных в очередь [ксреадпул](../../atl/reference/cthreadpool-class.md).

## <a name="members"></a>Элементы

### <a name="public-typedefs"></a>Общедоступные определения типов

|Имя|Описание|
|----------|-----------------|
|[Кнонстателессворкер:: RequestType](#requesttype)|Реализация [воркерарчетипе:: RequestType](worker-archetype.md#requesttype).|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кнонстателессворкер:: Execute](#execute)|Реализация [воркерарчетипе:: Execute](worker-archetype.md#execute).|
|[Кнонстателессворкер:: Initialize](#initialize)|Реализация [воркерарчетипе:: Initialize](worker-archetype.md#initialize).|
|[Кнонстателессворкер:: Terminate](#terminate)|Реализация [воркерарчетипе:: Terminate](worker-archetype.md#terminate).|

## <a name="remarks"></a>Комментарии

Этот класс является простым рабочим потоком для использования с [ксреадпул](../../atl/reference/cthreadpool-class.md). Этот класс не предоставляет собственные возможности обработки запросов. Вместо этого он создает экземпляр *Worker* на одном запросе и делегирует реализацию своих методов этому экземпляру.

Преимущество этого класса заключается в том, что он предоставляет удобный способ изменения модели состояний для существующих классов рабочих потоков. `CThreadPool` создает один рабочий процесс в течение времени существования потока, поэтому, если рабочий класс удерживает состояние, он будет удерживать его в нескольких запросах. Просто заключив этот класс в `CNonStatelessWorker` шаблон перед его использованием `CThreadPool` , время существования рабочей роли и состояние, которое он содержит, ограничено одним запросом.

## <a name="requirements"></a>Требования

**Заголовок:** файлов atlutil. h

## <a name="cnonstatelessworkerexecute"></a><a name="execute"></a> Кнонстателессворкер:: Execute

Реализация [воркерарчетипе:: Execute](worker-archetype.md#execute).

```cpp
void Execute(
    Worker::RequestType request,
    void* pvWorkerParam,
    OVERLAPPED* pOverlapped);
```

### <a name="remarks"></a>Комментарии

Этот метод создает экземпляр *рабочего* класса в стеке и вызывает метод [Initialize](worker-archetype.md#initialize) для этого объекта. Если инициализация прошла успешно, этот метод также вызывает [EXECUTE](worker-archetype.md#execute) и [Terminate](worker-archetype.md#terminate) для того же объекта.

## <a name="cnonstatelessworkerinitialize"></a><a name="initialize"></a> Кнонстателессворкер:: Initialize

Реализация [воркерарчетипе:: Initialize](worker-archetype.md#initialize).

```
BOOL Initialize(void* /* pvParam */) throw();
```

### <a name="return-value"></a>Возвращаемое значение

Всегда возвращает значение TRUE.

### <a name="remarks"></a>Комментарии

Этот класс не выполняет инициализацию в `Initialize` .

## <a name="cnonstatelessworkerrequesttype"></a><a name="requesttype"></a> Кнонстателессворкер:: RequestType

Реализация [воркерарчетипе:: RequestType](worker-archetype.md#requesttype).

```
typedef Worker::RequestType RequestType;
```

### <a name="remarks"></a>Комментарии

Этот класс обрабатывает тот же тип рабочего элемента, что и класс, используемый для параметра *рабочего* шаблона. Дополнительные сведения см. в [обзоре кнонстателессворкер](../../atl/reference/cnonstatelessworker-class.md) .

## <a name="cnonstatelessworkerterminate"></a><a name="terminate"></a> Кнонстателессворкер:: Terminate

Реализация [воркерарчетипе:: Terminate](worker-archetype.md#terminate).

```cpp
void Terminate(void* /* pvParam */) throw();
```

### <a name="remarks"></a>Комментарии

Этот класс не выполняет очистку в `Terminate` .

## <a name="see-also"></a>См. также раздел

[Класс Ксреадпул](../../atl/reference/cthreadpool-class.md)<br/>
[Архетипа рабочей роли](../../atl/reference/worker-archetype.md)<br/>
[Классы](../../atl/reference/atl-classes.md)
