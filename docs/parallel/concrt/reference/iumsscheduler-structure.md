---
description: 'Дополнительные сведения о: структура Иумссчедулер'
title: Структура IUMSScheduler
ms.date: 11/04/2016
f1_keywords:
- IUMSScheduler
- CONCRTRM/concurrency::IUMSScheduler
- CONCRTRM/concurrency::IUMSScheduler::IUMSScheduler::SetCompletionList
helpviewer_keywords:
- IUMSScheduler structure
ms.assetid: 3a500225-4e02-4849-bb56-d744865f5870
ms.openlocfilehash: e42a2e3d39e568ba12cd681053406ce88c7b5dba
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97334343"
---
# <a name="iumsscheduler-structure"></a>Структура IUMSScheduler

Интерфейс абстракции планировщика, которому требуется, чтобы диспетчер ресурсов среды выполнения с параллелизмом передал ему потоки планировщика в пользовательском режиме (UMS). Диспетчер ресурсов среды выполнения с параллелизмом использует этот интерфейс для взаимодействия с планировщиками потоков UMS. Интерфейс `IUMSScheduler` наследует от интерфейса `IScheduler` .

## <a name="syntax"></a>Синтаксис

```cpp
struct IUMSScheduler : public IScheduler;
```

## <a name="members"></a>Члены

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Иумссчедулер:: Сеткомплетионлист](#setcompletionlist)|Назначает `IUMSCompletionList` интерфейс планировщику потоков UMS.|

## <a name="remarks"></a>Комментарии

При реализации пользовательского планировщика, который взаимодействует с диспетчер ресурсов и требуется передать потоки UMS планировщику вместо обычных потоков Win32, необходимо предоставить реализацию `IUMSScheduler` интерфейса. Кроме того, необходимо задать для ключа политики планировщика значение `SchedulerKind` `UmsThreadDefault` . Если политика указывает UMS-поток, `IScheduler` интерфейс, передаваемый в качестве параметра в метод [метод IResourceManager:: регистерсчедулер](iresourcemanager-structure.md#registerscheduler) , должен быть `IUMSScheduler` интерфейсом.

Диспетчер ресурсов может передать вам UMS-потоки только в операционных системах, имеющих функцию UMS. 64-разрядные операционные системы с версиями Windows 7 и более поздней версии поддерживают UMS-потоки. Если вы создаете политику планировщика с `SchedulerKind` ключом, для которой задано значение, `UmsThreadDefault` а базовая платформа не поддерживает UMS, значение `SchedulerKind` ключа в этой политике будет изменено на значение `ThreadScheduler` . Необходимо всегда считывать это значение политики, прежде чем ожидать получения потоков UMS.

`IUMSScheduler`Интерфейс — это один конец двустороннего канала связи между планировщиком и диспетчер ресурсов. Другой конец представлен `IResourceManager` `ISchedulerProxy` интерфейсами и, которые реализуются диспетчер ресурсов.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[IScheduler](ischeduler-structure.md)

`IUMSScheduler`

## <a name="requirements"></a>Требования

**Заголовок:** concrtrm. h

**Пространство имен:** параллелизм

## <a name="iumsschedulersetcompletionlist-method"></a><a name="setcompletionlist"></a> Метод Иумссчедулер:: Сеткомплетионлист

Назначает `IUMSCompletionList` интерфейс планировщику потоков UMS.

```cpp
virtual void SetCompletionList(_Inout_ IUMSCompletionList* pCompletionList) = 0;
```

### <a name="parameters"></a>Параметры

*пкомплетионлист*<br/>
Интерфейс списка завершения для планировщика. Существует один список для каждого планировщика.

### <a name="remarks"></a>Комментарии

Диспетчер ресурсов вызовет этот метод для планировщика, который указывает, что требуется UMS-потоки, после того как планировщик запрашивает начальное выделение ресурсов. Планировщик может использовать `IUMSCompletionList` интерфейс, чтобы определить, когда были разблокированы прокси-серверы потоков UMS. Доступ к этому интерфейсу можно получить только из прокси-сервера потока, который работает на корневом виртуальном процессоре, назначенном планировщику UMS.

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency](concurrency-namespace.md)<br/>
[полициелементкэй](concurrency-namespace-enums.md)<br/>
[Структура IScheduler](ischeduler-structure.md)<br/>
[Структура IUMSCompletionList](iumscompletionlist-structure.md)<br/>
[Структура IResourceManager](iresourcemanager-structure.md)
