---
description: 'Дополнительные сведения о: Кноворкерсреад Class'
title: Класс Кноворкерсреад
ms.date: 11/04/2016
f1_keywords:
- CNoWorkerThread
- ATLUTIL/ATL::CNoWorkerThread
- ATLUTIL/ATL::CNoWorkerThread::AddHandle
- ATLUTIL/ATL::CNoWorkerThread::AddTimer
- ATLUTIL/ATL::CNoWorkerThread::GetThreadHandle
- ATLUTIL/ATL::CNoWorkerThread::GetThreadId
- ATLUTIL/ATL::CNoWorkerThread::Initialize
- ATLUTIL/ATL::CNoWorkerThread::RemoveHandle
- ATLUTIL/ATL::CNoWorkerThread::Shutdown
helpviewer_keywords:
- CNoWorkerThread class
ms.assetid: 29f06bae-b658-4aac-9c14-331e996d25d1
ms.openlocfilehash: 5159c04a8390f8933291f697faccedb7353fb48e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97141418"
---
# <a name="cnoworkerthread-class"></a>Класс Кноворкерсреад

Используйте этот класс в качестве аргумента для `MonitorClass` параметра шаблона для кэширования классов, если требуется отключить динамическое обслуживание кэша.

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```
class CNoWorkerThread
```

## <a name="members"></a>Члены

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кноворкерсреад:: Аддхандле](#addhandle)|Нефункциональный эквивалент [кворкерсреад:: аддхандле](../../atl/reference/cworkerthread-class.md#addhandle).|
|[Кноворкерсреад:: Аддтимер](#addtimer)|Нефункциональный эквивалент [кворкерсреад:: аддтимер](../../atl/reference/cworkerthread-class.md#addtimer).|
|[Кноворкерсреад:: Жетсреадхандле](#getthreadhandle)|Нефункциональный эквивалент [кворкерсреад:: жетсреадхандле](../../atl/reference/cworkerthread-class.md#getthreadhandle).|
|[Кноворкерсреад:: Жетсреадид](#getthreadid)|Нефункциональный эквивалент [кворкерсреад:: жетсреадид](../../atl/reference/cworkerthread-class.md#getthreadid).|
|[Кноворкерсреад:: Initialize](#initialize)|Нефункциональный эквивалент [кворкерсреад:: Initialize](../../atl/reference/cworkerthread-class.md#initialize).|
|[Кноворкерсреад:: Ремовехандле](#removehandle)|Нефункциональный эквивалент [кворкерсреад:: ремовехандле](../../atl/reference/cworkerthread-class.md#removehandle).|
|[Кноворкерсреад:: Shutdown](#shutdown)|Нефункциональный эквивалент [кворкерсреад:: Shutdown](../../atl/reference/cworkerthread-class.md#shutdown).|

## <a name="remarks"></a>Комментарии

Этот класс предоставляет тот же открытый интерфейс, что и [кворкерсреад](../../atl/reference/cworkerthread-class.md). Предполагается, что этот интерфейс предоставляется `MonitorClass` параметром шаблона для кэширования классов.

Методы в этом классе реализуются так, чтобы ничего не делать. Методы, возвращающие HRESULT, всегда возвращают S_OK, а методы, возвращающие маркер или идентификатор потока, всегда возвращают 0.

## <a name="requirements"></a>Требования

**Заголовок:** файлов atlutil. h

## <a name="cnoworkerthreadaddhandle"></a><a name="addhandle"></a> Кноворкерсреад:: Аддхандле

Нефункциональный эквивалент [кворкерсреад:: аддхандле](../../atl/reference/cworkerthread-class.md#addhandle).

```
HRESULT AddHandle(HANDLE /* hObject */,
    IWorkerThreadClient* /* pClient */,
    DWORD_PTR /* dwParam */) throw();
```

### <a name="return-value"></a>Возвращаемое значение

Всегда возвращает S_OK.

### <a name="remarks"></a>Комментарии

Реализация, предоставляемая этим классом, не выполняет никаких действий.

## <a name="cnoworkerthreadaddtimer"></a><a name="addtimer"></a> Кноворкерсреад:: Аддтимер

Нефункциональный эквивалент [кворкерсреад:: аддтимер](../../atl/reference/cworkerthread-class.md#addtimer).

```
HRESULT AddTimer(DWORD /* dwInterval */,
    IWorkerThreadClient* /* pClient */,
    DWORD_PTR /* dwParam */,
    HANDLE* /* phTimer */) throw();
```

### <a name="return-value"></a>Возвращаемое значение

Всегда возвращает S_OK.

### <a name="remarks"></a>Комментарии

Реализация, предоставляемая этим классом, не выполняет никаких действий.

## <a name="cnoworkerthreadgetthreadhandle"></a><a name="getthreadhandle"></a> Кноворкерсреад:: Жетсреадхандле

Нефункциональный эквивалент [кворкерсреад:: жетсреадхандле](../../atl/reference/cworkerthread-class.md#getthreadhandle).

```
HANDLE GetThreadHandle() throw();
```

### <a name="return-value"></a>Возвращаемое значение

Всегда возвращает значение NULL.

### <a name="remarks"></a>Комментарии

Реализация, предоставляемая этим классом, не выполняет никаких действий.

## <a name="cnoworkerthreadgetthreadid"></a><a name="getthreadid"></a> Кноворкерсреад:: Жетсреадид

Нефункциональный эквивалент [кворкерсреад:: жетсреадид](../../atl/reference/cworkerthread-class.md#getthreadid).

```
DWORD GetThreadId() throw();
```

### <a name="return-value"></a>Возвращаемое значение

Всегда возвращает 0.

### <a name="remarks"></a>Комментарии

Реализация, предоставляемая этим классом, не выполняет никаких действий.

## <a name="cnoworkerthreadinitialize"></a><a name="initialize"></a> Кноворкерсреад:: Initialize

Нефункциональный эквивалент [кворкерсреад:: Initialize](../../atl/reference/cworkerthread-class.md#initialize).

```
HRESULT Initialize() throw();
```

### <a name="return-value"></a>Возвращаемое значение

Всегда возвращает S_OK.

### <a name="remarks"></a>Комментарии

Реализация, предоставляемая этим классом, не выполняет никаких действий.

## <a name="cnoworkerthreadremovehandle"></a><a name="removehandle"></a> Кноворкерсреад:: Ремовехандле

Нефункциональный эквивалент [кворкерсреад:: ремовехандле](../../atl/reference/cworkerthread-class.md#removehandle).

```
HRESULT RemoveHandle(HANDLE /* hObject */) throw();
```

### <a name="return-value"></a>Возвращаемое значение

Всегда возвращает S_OK.

### <a name="remarks"></a>Комментарии

Реализация, предоставляемая этим классом, не выполняет никаких действий.

## <a name="cnoworkerthreadshutdown"></a><a name="shutdown"></a> Кноворкерсреад:: Shutdown

Нефункциональный эквивалент [кворкерсреад:: Shutdown](../../atl/reference/cworkerthread-class.md#shutdown).

```
HRESULT Shutdown(DWORD dwWait = ATL_WORKER_THREAD_WAIT) throw();
```

### <a name="return-value"></a>Возвращаемое значение

Всегда возвращает S_OK.

### <a name="remarks"></a>Комментарии

Реализация, предоставляемая этим классом, не выполняет никаких действий.
