---
description: 'Дополнительные сведения: Worker архетипа'
title: Архетипа рабочей роли
ms.date: 11/04/2016
helpviewer_keywords:
- Worker archetype
ms.assetid: 834145cd-09d3-4149-bc99-620e1871cbfb
ms.openlocfilehash: 8cb8c2b281bbdc074bb700b77a856f4d26c26cf6
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97157572"
---
# <a name="worker-archetype"></a>Архетипа рабочей роли

Классы, которые соответствуют *рабочей* архетипа, предоставляют код для обработки рабочих элементов, помещенных в очередь пула потоков.

**Реализация**

Чтобы реализовать класс, который соответствует этому архетипа, класс должен предоставить следующие возможности:

|Метод|Описание|
|------------|-----------------|
|[Инициализация](#initialize)|Вызывается для инициализации рабочего объекта перед передачей [выполнения](#execute)любых запросов.|
|[Execute](#execute)|Вызывается для обработки рабочего элемента.|
|[Завершение](#terminate)|Вызывается для деинициализации рабочего объекта после того, как все запросы были переданы для [выполнения](#execute).|

|Typedef|Описание|
|-------------|-----------------|
|[RequestType](#requesttype)|Определение типа рабочего элемента, которое может быть обработано рабочим классом.|

Типичный *Рабочий* класс выглядит следующим образом:

[!code-cpp[NVC_ATL_Utilities#137](../../atl/codesnippet/cpp/worker-archetype_1.cpp)]

**Существующие реализации**

Эти классы соответствуют этому архетипа:

|Класс|Описание|
|-----------|-----------------|
|[кнонстателессворкер](../../atl/reference/cnonstatelessworker-class.md)|Получает запросы из пула потоков и передает их в рабочий объект, который создается и уничтожается для каждого запроса.|

**Использование**

Эти параметры шаблона предполагают, что класс должен соответствовать этому архетипа:

|Имя параметра|Где используется|
|--------------------|-------------|
|*Рабочий узел*|[CThreadPool](../../atl/reference/cthreadpool-class.md)|
|*Рабочий узел*|[кнонстателессворкер](../../atl/reference/cnonstatelessworker-class.md)|

### <a name="requirements"></a>Требования

**Заголовок:** файлов atlutil. h

## <a name="workerarchetypeexecute"></a><a name="execute"></a> Воркерарчетипе:: Execute

Вызывается для обработки рабочего элемента.

```cpp
void Execute(
    RequestType request,
    void* pvWorkerParam,
    OVERLAPPED* pOverlapped);
```

#### <a name="parameters"></a>Параметры

*request*<br/>
Рабочий элемент для обработки. Рабочий элемент имеет тот же тип, что и `RequestType` .

*пвворкерпарам*<br/>
Пользовательский параметр, понятный рабочему классу. Также передается в `WorkerArchetype::Initialize` и `Terminate` .

*поверлаппед*<br/>
Указатель на структуру [OVERLAPPED](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) , используемую для создания очереди, в которой были поставлены рабочие элементы.

## <a name="workerarchetypeinitialize"></a><a name="initialize"></a> Воркерарчетипе:: Initialize

Вызывается для инициализации рабочего объекта перед передачей запросов `WorkerArchetype::Execute` .

```
BOOL Initialize(void* pvParam) throw();
```

#### <a name="parameters"></a>Параметры

*пвпарам*<br/>
Пользовательский параметр, понятный рабочему классу. Также передается в `WorkerArchetype::Terminate` и `WorkerArchetype::Execute` .

### <a name="return-value"></a>Возвращаемое значение

Возврат значения TRUE при успешном выполнении, FALSE при сбое.

## <a name="workerarchetyperequesttype"></a><a name="requesttype"></a> Воркерарчетипе:: RequestType

Определение типа рабочего элемента, которое может быть обработано рабочим классом.

```
typedef MyRequestType RequestType;
```

### <a name="remarks"></a>Комментарии

Этот тип должен использоваться в качестве первого параметра `WorkerArchetype::Execute` и должен поддерживать приведение к ULONG_PTR и из него.

## <a name="workerarchetypeterminate"></a><a name="terminate"></a> Воркерарчетипе:: Terminate

Вызывается для деинициализации рабочего объекта после передачи всех запросов в `WorkerArchetype::Execute` ).

```cpp
void Terminate(void* pvParam) throw();
```

#### <a name="parameters"></a>Параметры

*пвпарам*<br/>
Пользовательский параметр, понятный рабочему классу. Также передается в `WorkerArchetype::Initialize` и `WorkerArchetype::Execute` .

## <a name="see-also"></a>См. также раздел

[Основные понятия](../../atl/active-template-library-atl-concepts.md)<br/>
[Компоненты ATL COM Desktop](../../atl/atl-com-desktop-components.md)
