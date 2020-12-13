---
description: 'Дополнительные сведения о: структура метод iumsthreadproxy'
title: Структура IUMSThreadProxy
ms.date: 11/04/2016
f1_keywords:
- IUMSThreadProxy
- CONCRTRM/concurrency::IUMSThreadProxy
- CONCRTRM/concurrency::IUMSThreadProxy::IUMSThreadProxy::EnterCriticalRegion
- CONCRTRM/concurrency::IUMSThreadProxy::IUMSThreadProxy::EnterHyperCriticalRegion
- CONCRTRM/concurrency::IUMSThreadProxy::IUMSThreadProxy::ExitCriticalRegion
- CONCRTRM/concurrency::IUMSThreadProxy::IUMSThreadProxy::ExitHyperCriticalRegion
- CONCRTRM/concurrency::IUMSThreadProxy::IUMSThreadProxy::GetCriticalRegionType
helpviewer_keywords:
- IUMSThreadProxy structure
ms.assetid: 61c69b7e-5c37-4048-bcb4-e75c536afd86
ms.openlocfilehash: 02eb999b35143e4fc9e0416e02abb60c3c64768d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97334328"
---
# <a name="iumsthreadproxy-structure"></a>Структура IUMSThreadProxy

Абстракция для потока выполнения. Если требуется предоставлять для планировщика потоки планировщика в пользовательском режиме (UMS), задайте для элемента политики планировщика `SchedulerKind` значение `UmsThreadDefault` и реализуйте интерфейс `IUMSScheduler`. Потоки UMS поддерживаются только в 64-разрядных операционных системах Windows 7 и более поздних версий.

## <a name="syntax"></a>Синтаксис

```cpp
struct IUMSThreadProxy : public IThreadProxy;
```

## <a name="members"></a>Члены

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Метод iumsthreadproxy:: Ентеркритикалрегион](#entercriticalregion)|Вызывается для входа в критическую область. В критической области планировщик не будет наблюдать за операциями асинхронной блокировки, происходящими в этом регионе. Это означает, что планировщик не будет повторно введен для ошибок страниц, приостановки потоков, асинхронных вызовов процедур ядра (APC) и т. д. для потока UMS.|
|[Метод iumsthreadproxy:: Ентерхиперкритикалрегион](#enterhypercriticalregion)|Вызывается для входа в область, критическая для Hyper. В области, критической для Hyper, планировщик не будет наблюдать за операциями блокировки, происходящими в этом регионе. Это означает, что в планировщик не будет повторных входов для блокирующих вызовов функции, блокирующих попыток получения блокировки, сбоев страниц, приостановок потока, вызовов асинхронных процедур ядра (APC) и т. п. для потока UMS.|
|[Метод iumsthreadproxy:: Екситкритикалрегион](#exitcriticalregion)|Вызывается для выхода из критической области.|
|[Метод iumsthreadproxy:: Ексисиперкритикалрегион](#exithypercriticalregion)|Вызывается для выхода из области, критической для Hyper.|
|[Метод iumsthreadproxy:: Жеткритикалрегионтипе](#getcriticalregiontype)|Возвращает тип критической области, в которой находится прокси-сервер потока. Поскольку регионы, критические с помощью Hyper-in, представляют собой надмножество критических регионов, если код вошел в критическую область, а затем будет возвращена критическая для Hyper-in область `InsideHyperCriticalRegion` .|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[исреадпрокси](ithreadproxy-structure.md)

`IUMSThreadProxy`

## <a name="requirements"></a>Требования

**Заголовок:** concrtrm. h

**Пространство имен:** параллелизм

## <a name="iumsthreadproxyentercriticalregion-method"></a><a name="entercriticalregion"></a> Метод метод iumsthreadproxy:: Ентеркритикалрегион

Вызывается для входа в критическую область. В критической области планировщик не будет наблюдать за операциями асинхронной блокировки, происходящими в этом регионе. Это означает, что планировщик не будет повторно введен для ошибок страниц, приостановки потоков, асинхронных вызовов процедур ядра (APC) и т. д. для потока UMS.

```cpp
virtual int EnterCriticalRegion() = 0;
```

### <a name="return-value"></a>Возвращаемое значение

Новая глубина критической области. Критические регионы — это повторные входы.

## <a name="iumsthreadproxyenterhypercriticalregion-method"></a><a name="enterhypercriticalregion"></a> Метод метод iumsthreadproxy:: Ентерхиперкритикалрегион

Вызывается для входа в область, критическая для Hyper. В области, критической для Hyper, планировщик не будет наблюдать за операциями блокировки, происходящими в этом регионе. Это означает, что в планировщик не будет повторных входов для блокирующих вызовов функции, блокирующих попыток получения блокировки, сбоев страниц, приостановок потока, вызовов асинхронных процедур ядра (APC) и т. п. для потока UMS.

```cpp
virtual int EnterHyperCriticalRegion() = 0;
```

### <a name="return-value"></a>Возвращаемое значение

Новая глубина критической для Hyper-безопасности области. Области, критические для Hyper, — это повторный вход.

### <a name="remarks"></a>Комментарии

Планировщик должен быть чрезвычайно осторожность о том, какие методы он вызывает, и какие блокировки он получает в таких регионах. Если код в таком регионе блокирует блокировку, которая удерживается каким-либо планировщиком, то может возникнуть взаимоблокировка.

## <a name="iumsthreadproxyexitcriticalregion-method"></a><a name="exitcriticalregion"></a> Метод метод iumsthreadproxy:: Екситкритикалрегион

Вызывается для выхода из критической области.

```cpp
virtual int ExitCriticalRegion() = 0;
```

### <a name="return-value"></a>Возвращаемое значение

Новая глубина критической области. Критические регионы — это повторные входы.

## <a name="iumsthreadproxyexithypercriticalregion-method"></a><a name="exithypercriticalregion"></a> Метод метод iumsthreadproxy:: Ексисиперкритикалрегион

Вызывается для выхода из области, критической для Hyper.

```cpp
virtual int ExitHyperCriticalRegion() = 0;
```

### <a name="return-value"></a>Возвращаемое значение

Новая глубина критической для Hyper-безопасности области. Области, критические для Hyper, — это повторный вход.

## <a name="iumsthreadproxygetcriticalregiontype-method"></a><a name="getcriticalregiontype"></a> Метод метод iumsthreadproxy:: Жеткритикалрегионтипе

Возвращает тип критической области, в которой находится прокси-сервер потока. Поскольку регионы, критические с помощью Hyper-in, представляют собой надмножество критических регионов, если код вошел в критическую область, а затем будет возвращена критическая для Hyper-in область `InsideHyperCriticalRegion` .

```cpp
virtual CriticalRegionType GetCriticalRegionType() const = 0;
```

### <a name="return-value"></a>Возвращаемое значение

Тип критической области, в которой находится прокси-объект потока.

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency](concurrency-namespace.md)<br/>
[Структура IUMSScheduler](iumsscheduler-structure.md)
