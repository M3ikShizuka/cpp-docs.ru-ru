---
description: 'Дополнительные сведения о: структура Иумсунблоккнотификатион'
title: Структура IUMSUnblockNotification
ms.date: 11/04/2016
f1_keywords:
- IUMSUnblockNotification
- CONCRTRM/concurrency::IUMSUnblockNotification
- CONCRTRM/concurrency::IUMSUnblockNotification::IUMSUnblockNotification::GetContext
- CONCRTRM/concurrency::IUMSUnblockNotification::IUMSUnblockNotification::GetNextUnblockNotification
helpviewer_keywords:
- IUMSUnblockNotification structure
ms.assetid: eaca9529-c1cc-472b-8ec6-722a1ff0fa2a
ms.openlocfilehash: bec40ee1e7326ad37e205c3035f965cb3f0ec8d4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97334310"
---
# <a name="iumsunblocknotification-structure"></a>Структура IUMSUnblockNotification

Представляет уведомление диспетчера ресурсов о том, что прокси-поток, который заблокировал и запустил возврат к заданному контексту планирования планировщика, разблокирован и готов для планирования. Этот интерфейс является недопустимым, когда связанный с прокси-потоком контекст выполнения, возвращенный из метода `GetContext`, переносится.

## <a name="syntax"></a>Синтаксис

```cpp
struct IUMSUnblockNotification;
```

## <a name="members"></a>Члены

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Иумсунблоккнотификатион:: SPContext](#getcontext)|Возвращает `IExecutionContext` интерфейс для контекста выполнения, связанного с прокси-сервером потока, который был разблокирован. После того как этот метод возвращает управление, а базовый контекст выполнения был перепланирован с помощью вызова `IThreadProxy::SwitchTo` метода, этот интерфейс больше не является допустимым.|
|[Иумсунблоккнотификатион:: Жетнекстунблоккнотификатион](#getnextunblocknotification)|Возвращает следующий `IUMSUnblockNotification` интерфейс в цепочке, возвращенной методом `IUMSCompletionList::GetUnblockNotifications` .|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`IUMSUnblockNotification`

## <a name="requirements"></a>Требования

**Заголовок:** concrtrm. h

**Пространство имен:** параллелизм

## <a name="iumsunblocknotificationgetcontext-method"></a><a name="getcontext"></a> Метод Иумсунблоккнотификатион:: oncontext

Возвращает `IExecutionContext` интерфейс для контекста выполнения, связанного с прокси-сервером потока, который был разблокирован. После того как этот метод возвращает управление, а базовый контекст выполнения был перепланирован с помощью вызова `IThreadProxy::SwitchTo` метода, этот интерфейс больше не является допустимым.

```cpp
virtual IExecutionContext* GetContext() = 0;
```

### <a name="return-value"></a>Возвращаемое значение

`IExecutionContext`Интерфейс для контекста выполнения для прокси-сервера потока, который был разблокирован.

## <a name="iumsunblocknotificationgetnextunblocknotification-method"></a><a name="getnextunblocknotification"></a> Метод Иумсунблоккнотификатион:: Жетнекстунблоккнотификатион

Возвращает следующий `IUMSUnblockNotification` интерфейс в цепочке, возвращенной методом `IUMSCompletionList::GetUnblockNotifications` .

```cpp
virtual IUMSUnblockNotification* GetNextUnblockNotification() = 0;
```

### <a name="return-value"></a>Возвращаемое значение

Следующий `IUMSUnblockNotification` интерфейс в цепочке, возвращенной методом `IUMSCompletionList::GetUnblockNotifications` .

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency](concurrency-namespace.md)<br/>
[Структура IUMSScheduler](iumsscheduler-structure.md)<br/>
[Структура IUMSCompletionList](iumscompletionlist-structure.md)
