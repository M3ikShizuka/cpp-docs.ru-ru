---
description: 'Дополнительные сведения о: IDispatchImpl Class'
title: Класс IDispatchImpl
ms.date: 11/04/2016
f1_keywords:
- IDispatchImpl
- ATLCOM/ATL::IDispatchImpl
- ATLCOM/ATL::IDispatchImpl::IDispatchImpl
- ATLCOM/ATL::IDispatchImpl::GetIDsOfNames
- ATLCOM/ATL::IDispatchImpl::GetTypeInfo
- ATLCOM/ATL::IDispatchImpl::GetTypeInfoCount
- ATLCOM/ATL::IDispatchImpl::Invoke
helpviewer_keywords:
- dual interfaces, classes
- IDispatchImpl class
- IDispatch class support in ATL
ms.assetid: 8108eb36-1228-4127-a203-3ab5ba488892
ms.openlocfilehash: 709b703bf610776191b2587d11a0c5be651c4938
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97139559"
---
# <a name="idispatchimpl-class"></a>Класс IDispatchImpl

Предоставляет реализацию по умолчанию для `IDispatch` части сдвоенного интерфейса.

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```
template<class T,
        const IID* piid= &__uuidof(T),
        const GUID* plibid = &CAtlModule::m_libid,
        WORD wMajor = 1,
        WORD wMinor = 0,
        class tihclass = CComTypeInfoHolder>
class ATL_NO_VTABLE IDispatchImpl : public T
```

#### <a name="parameters"></a>Параметры

*T*<br/>
окне Сдвоенный интерфейс.

*пиид*<br/>
окне Указатель на идентификатор IID объекта *T*.

*плибид*<br/>
окне Указатель на идентификатор LIBID библиотеки типов, который содержит сведения об интерфейсе. По умолчанию передается библиотека типов на уровне сервера.

*вмажор*<br/>
окне Основной номер версии библиотеки типов. Значение по умолчанию — 1.

*вминор*<br/>
окне Дополнительный номер версии библиотеки типов. По умолчанию значение равно 0.

*тихкласс*<br/>
окне Класс, используемый для управления сведениями о типе для *T*. По умолчанию используется значение `CComTypeInfoHolder` .

## <a name="members"></a>Элементы

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[IDispatchImpl:: IDispatchImpl](#idispatchimpl)|Конструктор. Вызывает `AddRef` в защищенной переменной члена, которая управляет сведениями о типе для сдвоенного интерфейса. Деструктор вызывает `Release`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[IDispatchImpl:: GetIDsOfNames](#getidsofnames)|Сопоставляет набор имен соответствующему набору идентификаторов диспетчеризации.|
|[IDispatchImpl:: GetTypeInfo](#gettypeinfo)|Извлекает сведения о типе для сдвоенного интерфейса.|
|[IDispatchImpl:: Жеттипеинфокаунт](#gettypeinfocount)|Определяет, доступны ли сведения о типе для сдвоенного интерфейса.|
|[IDispatchImpl:: Invoke](#invoke)|Предоставляет доступ к методам и свойствам, предоставляемым сдвоенным интерфейсом.|

## <a name="remarks"></a>Комментарии

`IDispatchImpl` предоставляет реализацию по умолчанию для `IDispatch` части любого сдвоенного интерфейса в объекте. Сдвоенный интерфейс является производным от `IDispatch` и использует только типы, совместимые с автоматизацией. Как и диспетчерский интерфейс, сдвоенный интерфейс поддерживает раннее связывание и позднее связывание. Однако сдвоенный интерфейс также поддерживает привязку vtable.

В следующем примере показана типичная реализация `IDispatchImpl` .

[!code-cpp[NVC_ATL_COM#47](../../atl/codesnippet/cpp/idispatchimpl-class_1.h)]

По умолчанию `IDispatchImpl` класс ищет в реестре сведения о типе для *T* . Для реализации незарегистрированного интерфейса можно использовать `IDispatchImpl` класс без доступа к реестру с помощью предопределенного номера версии. При создании `IDispatchImpl` объекта с 0xFFFF в качестве значения для *Вмажор* и 0xFFFF в качестве значения для *вминор* `IDispatchImpl` класс получает библиотеку типов из DLL-файла, а не из реестра.

`IDispatchImpl` содержит статический элемент типа `CComTypeInfoHolder` , который управляет сведениями о типе для сдвоенного интерфейса. При наличии нескольких объектов, реализующих один и тот же сдвоенный интерфейс, используется только один экземпляр `CComTypeInfoHolder` .

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`T`

`IDispatchImpl`

## <a name="requirements"></a>Требования

**Заголовок:** атлком. h

## <a name="idispatchimplgetidsofnames"></a><a name="getidsofnames"></a> IDispatchImpl:: GetIDsOfNames

Сопоставляет набор имен соответствующему набору идентификаторов диспетчеризации.

```
STDMETHOD(GetIDsOfNames)(
    REFIID riid,
    LPOLESTR* rgszNames,
    UINT cNames,
    LCID lcid,
    DISPID* rgdispid);
```

### <a name="remarks"></a>Комментарии

См. раздел [IDispatch:: GetIdsOfNames](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) в Windows SDK.

## <a name="idispatchimplgettypeinfo"></a><a name="gettypeinfo"></a> IDispatchImpl:: GetTypeInfo

Извлекает сведения о типе для сдвоенного интерфейса.

```
STDMETHOD(GetTypeInfo)(
    UINT itinfo,
    LCID lcid,
    ITypeInfo** pptinfo);
```

### <a name="remarks"></a>Комментарии

См. раздел [IDispatch:: GetTypeInfo](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo) в Windows SDK.

## <a name="idispatchimplgettypeinfocount"></a><a name="gettypeinfocount"></a> IDispatchImpl:: Жеттипеинфокаунт

Определяет, доступны ли сведения о типе для сдвоенного интерфейса.

```
STDMETHOD(GetTypeInfoCount)(UINT* pctinfo);
```

### <a name="remarks"></a>Комментарии

См `IDispatch::GetTypeInfoCount` . раздел Windows SDK.

## <a name="idispatchimplidispatchimpl"></a><a name="idispatchimpl"></a> IDispatchImpl:: IDispatchImpl

Конструктор. Вызывает `AddRef` в защищенной переменной члена, которая управляет сведениями о типе для сдвоенного интерфейса. Деструктор вызывает `Release`.

```
IDispatchImpl();
```

## <a name="idispatchimplinvoke"></a><a name="invoke"></a> IDispatchImpl:: Invoke

Предоставляет доступ к методам и свойствам, предоставляемым сдвоенным интерфейсом.

```
STDMETHOD(Invoke)(
    DISPID dispidMember,
    REFIID riid,
    LCID lcid,
    WORD wFlags,
    DISPPARAMS* pdispparams,
    VARIANT* pvarResult,
    EXCEPINFO* pexcepinfo,
    UINT* puArgErr);
```

### <a name="remarks"></a>Комментарии

См. раздел [IDispatch:: Invoke](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) в Windows SDK.

## <a name="see-also"></a>См. также раздел

[Общие сведения о классах](../../atl/atl-class-overview.md)
