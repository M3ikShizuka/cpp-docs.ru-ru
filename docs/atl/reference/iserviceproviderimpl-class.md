---
description: 'Дополнительные сведения о: Исервицепровидеримпл Class'
title: Класс Исервицепровидеримпл
ms.date: 11/04/2016
f1_keywords:
- IServiceProviderImpl
- ATLCOM/ATL::IServiceProviderImpl
- ATLCOM/ATL::IServiceProviderImpl::QueryService
helpviewer_keywords:
- IServiceProviderImpl class
- IServiceProvider interface, ATL implementation
ms.assetid: 251254d3-c4ce-40d7-aee0-3d676d1d72f2
ms.openlocfilehash: 0cd9fab784fe8bffe420123129aa51c80c187890
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97139156"
---
# <a name="iserviceproviderimpl-class"></a>Класс Исервицепровидеримпл

Этот класс предоставляет реализацию интерфейса по умолчанию `IServiceProvider` .

## <a name="syntax"></a>Синтаксис

```
template <class T>
class ATL_NO_VTABLE IServiceProviderImpl : public IServiceProvider
```

#### <a name="parameters"></a>Параметры

*T*<br/>
Класс, производный от `IServiceProviderImpl` .

## <a name="members"></a>Элементы

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Исервицепровидеримпл:: QueryService](#queryservice)|Создает или обращается к указанной службе и возвращает указатель интерфейса на указанный интерфейс для службы.|

## <a name="remarks"></a>Комментарии

`IServiceProvider`Интерфейс находит службу, указанную по ее идентификатору GUID, и возвращает указатель интерфейса для запрошенного интерфейса службы. Класс `IServiceProviderImpl` предоставляет реализацию по умолчанию для этого интерфейса.

`IServiceProviderImpl` Указывает один метод: [QueryService](#queryservice), который создает или обращается к указанной службе и возвращает указатель интерфейса на указанный интерфейс для службы.

`IServiceProviderImpl` использует схему услуги, начиная с [BEGIN_SERVICE_MAP](service-map-macros.md#begin_service_map) и заканчивая [END_SERVICE_MAP](service-map-macros.md#end_service_map).

Схема услуги содержит две записи: [SERVICE_ENTRY](service-map-macros.md#service_entry), указывающие указанный идентификатор службы (SID), поддерживаемый объектом, и [SERVICE_ENTRY_CHAIN](service-map-macros.md#service_entry_chain), который вызывает `QueryService` цепочку для другого объекта.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`IServiceProvider`

`IServiceProviderImpl`

## <a name="requirements"></a>Требования

**Заголовок:** атлком. h

## <a name="iserviceproviderimplqueryservice"></a><a name="queryservice"></a> Исервицепровидеримпл:: QueryService

Создает или обращается к указанной службе и возвращает указатель интерфейса на указанный интерфейс для службы.

```
STDMETHOD(QueryService)(
    REFGUID guidService,
    REFIID riid,
    void** ppvObject);
```

### <a name="parameters"></a>Параметры

*гуидсервице*<br/>
окне Указатель на идентификатор службы (SID).

*riid*<br/>
окне Идентификатор интерфейса, к которому вызывающий объект должен получить доступ.

*ппвобж*<br/>
заполняет Косвенный указатель на запрошенный интерфейс.

### <a name="return-value"></a>Возвращаемое значение

Возвращенное значение HRESULT является одним из следующих:

|Возвращаемое значение|Значение|
|------------------|-------------|
|S_OK|Служба успешно создана или получена.|
|E_INVALIDARG|Один или несколько аргументов являются недопустимыми.|
|E_OUTOFMEMORY|Недостаточно памяти для создания службы.|
|E_UNEXPECTED|Произошла неизвестная ошибка.|
|E_NOINTERFACE|Запрошенный интерфейс не является частью этой службы, или служба неизвестна.|

### <a name="remarks"></a>Комментарии

`QueryService` Возвращает непрямой указатель на запрошенный интерфейс в указанной службе. Вызывающий объект отвечает за освобождение этого указателя, когда он больше не требуется.

При вызове `QueryService` вы передаете идентификатор службы (*гуидсервице*) и идентификатор интерфейса (*riid*). *Гуидсервице* указывает службу, к которой необходимо получить доступ, а *riid* определяет интерфейс, который является частью службы. В случае возврата вы получаете косвенный указатель на интерфейс.

Объект, реализующий интерфейс, может также реализовывать интерфейсы, которые являются частью других служб. Рассмотрим следующий пример.

- Некоторые из этих интерфейсов могут быть необязательными. Не все интерфейсы, определенные в описании службы, всегда приводятся при каждой реализации службы или при каждом возвращенном объекте.

- В отличие от вызовов `QueryInterface` , передача другого идентификатора службы не обязательно означает, что возвращается другой объект модели COM.

- Возвращаемый объект может иметь дополнительные интерфейсы, не входящие в определение службы.

Две различные службы, такие как SID_SMyService и SID_SYourService, могут указывать использование одного интерфейса, даже несмотря на то, что реализация интерфейса может вообще не иметь ничего общего между двумя службами. Это работает, поскольку вызов `QueryService` (SID_SMyService, IID_IDispatch) может возвращать другой объект, чем `QueryService` (SID_SYourService, IID_IDispatch). При указании другого идентификатора службы удостоверение объекта не предполагается.

## <a name="see-also"></a>См. также раздел

[Общие сведения о классах](../../atl/atl-class-overview.md)
