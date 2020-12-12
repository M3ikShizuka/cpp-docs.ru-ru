---
description: 'Дополнительные сведения о: метод ActivationFactory Class'
title: ActivationFactory - класс
ms.date: 10/03/2018
ms.topic: reference
f1_keywords:
- module/Microsoft::WRL::ActivationFactory
- module/Microsoft::WRL::ActivationFactory::ActivationFactory
- module/Microsoft::WRL::ActivationFactory::AddRef
- module/Microsoft::WRL::ActivationFactory::GetIids
- module/Microsoft::WRL::ActivationFactory::GetRuntimeClassName
- module/Microsoft::WRL::ActivationFactory::GetTrustLevel
- module/Microsoft::WRL::ActivationFactory::QueryInterface
- module/Microsoft::WRL::ActivationFactory::Release
helpviewer_keywords:
- Microsoft::WRL::ActivationFactory class
- Microsoft::WRL::ActivationFactory::ActivationFactory, constructor
- Microsoft::WRL::ActivationFactory::AddRef method
- Microsoft::WRL::ActivationFactory::GetIids method
- Microsoft::WRL::ActivationFactory::GetRuntimeClassName method
- Microsoft::WRL::ActivationFactory::GetTrustLevel method
- Microsoft::WRL::ActivationFactory::QueryInterface method
- Microsoft::WRL::ActivationFactory::Release method
ms.assetid: 5faddf1f-43b6-4f8a-97de-8c9d3ae1e1ff
ms.openlocfilehash: 7204a3c2f981947a03efba648dd91b69d582fee1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97287844"
---
# <a name="activationfactory-class"></a>ActivationFactory - класс

Позволяет одному или нескольким классам быть активированными средой выполнения Windows.

## <a name="syntax"></a>Синтаксис

```cpp
template <
    typename I0 = Details::Nil,
    typename I1 = Details::Nil,
    typename I2 = Details::Nil
>
class ActivationFactory :
    public Details::RuntimeClass<
        typename Details::InterfaceListHelper<
            IActivationFactory,
            I0,
            I1,
            I2,
            Details::Nil
        >::TypeT,
        RuntimeClassFlags<WinRt | InhibitWeakReference>,
        false
    >;
```

### <a name="parameters"></a>Параметры

*I0*<br/>
Интерфейс начальном.

*I1*<br/>
Первый интерфейс.

*I2*<br/>
Второй интерфейс.

## <a name="remarks"></a>Комментарии

`ActivationFactory` предоставляет методы регистрации и базовые функциональные возможности для `IActivationFactory` интерфейса. `ActivationFactory` также позволяет предоставить собственную реализацию фабрики.

В следующем фрагменте кода показано, как использовать метод ActivationFactory.

[!code-cpp[wrl-microsoft__wrl__activationfactory#1](../codesnippet/CPP/activationfactory-class_1.cpp)]

В следующем фрагменте кода показано, как использовать структуру [Implements](implements-structure.md) , чтобы указать более трех идентификаторов интерфейса.

`struct MyFactory : ActivationFactory<Implements<I1, I2, I3>, I4, I5>;`

## <a name="members"></a>Элементы

### <a name="public-constructors"></a>Открытые конструкторы

name                                                       | Описание
---------------------------------------------------------- | ------------------------------------------
[Метод ActivationFactory:: метод ActivationFactory](#activationfactory) | Инициализирует класс `ActivationFactory`.

### <a name="public-methods"></a>Открытые методы

name                                                           | Описание
-------------------------------------------------------------- | --------------------------------------------------------------------------------------------
[Метод ActivationFactory:: AddRef](#addref)                           | Увеличивает значение счетчика ссылок текущего `ActivationFactory` объекта.
[Метод ActivationFactory:: GetIids](#getiids)                         | Извлекает массив идентификаторов реализованного интерфейса.
[Метод ActivationFactory:: GetRuntimeClassName](#getruntimeclassname) | Возвращает имя класса среды выполнения для объекта, который является текущим `ActivationFactory` экземпляром.
[Метод ActivationFactory:: GetTrustLevel](#gettrustlevel)             | Возвращает уровень доверия объекта, который является текущим `ActivationFactory` экземпляром.
[Метод ActivationFactory:: QueryInterface](#queryinterface)           | Извлекает указатель на указанный интерфейс.
[Метод ActivationFactory:: Release](#release)                         | Уменьшает значение счетчика ссылок текущего `ActivationFactory` объекта.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`I0`

`ChainInterfaces`

`I0`

`RuntimeClassBase`

`ImplementsHelper`

`DontUseNewUseMake`

`RuntimeClassFlags`

`RuntimeClassBaseT`

`RuntimeClass`

`ActivationFactory`

## <a name="requirements"></a>Требования

**Заголовок:** Module. h

**Пространство имен:** Microsoft::WRL

## <a name="activationfactoryactivationfactory"></a><a name="activationfactory"></a> Метод ActivationFactory:: метод ActivationFactory

Инициализирует класс `ActivationFactory`.

```cpp
ActivationFactory();
```

## <a name="activationfactoryaddref"></a><a name="addref"></a> Метод ActivationFactory:: AddRef

Увеличивает значение счетчика ссылок текущего `ActivationFactory` объекта.

```cpp
STDMETHOD_(
   ULONG,
   AddRef
)();
```

### <a name="return-value"></a>Возвращаемое значение

Значение S_OK, если операция завершилась успешно; в противном случае — значение HRESULT, описывающее тип сбоя.

## <a name="activationfactorygetiids"></a><a name="getiids"></a> Метод ActivationFactory:: GetIids

Извлекает массив идентификаторов реализованного интерфейса.

```cpp
STDMETHOD(
   GetIids
)(_Out_ ULONG *iidCount, _Deref_out_ _Deref_post_cap_(*iidCount) IID **iids);
```

### <a name="parameters"></a>Параметры

*iidCount*<br/>
По завершении этой операции число идентификаторов свойства интерфейса в массиве *идентификаторов IID* .

*идентификаторов IID*<br/>
После завершения операции представляет массив идентификаторов реализованного интерфейса.

### <a name="return-value"></a>Возвращаемое значение

Значение S_OK, если операция завершилась успешно; в противном случае — значение HRESULT, описывающее тип сбоя. E_OUTOFMEMORY является возможной ошибкой HRESULT.

## <a name="activationfactorygetruntimeclassname"></a><a name="getruntimeclassname"></a> Метод ActivationFactory:: GetRuntimeClassName

Возвращает имя класса среды выполнения для объекта, который является текущим `ActivationFactory` экземпляром.

```cpp
STDMETHOD(
   GetRuntimeClassName
)(_Out_ HSTRING* runtimeName);
```

### <a name="parameters"></a>Параметры

*рунтименаме*<br/>
По завершении этой операции — обработчик строки, содержащей имя класса среды выполнения для объекта, который является текущим `ActivationFactory` экземпляром.

### <a name="return-value"></a>Возвращаемое значение

Значение S_OK, если операция завершилась успешно; в противном случае — значение HRESULT, описывающее тип сбоя.

## <a name="activationfactorygettrustlevel"></a><a name="gettrustlevel"></a> Метод ActivationFactory:: GetTrustLevel

Возвращает уровень доверия объекта, который является текущим `ActivationFactory` экземпляром.

```cpp
STDMETHOD(
   GetTrustLevel
)(_Out_ TrustLevel* trustLvl);
```

### <a name="parameters"></a>Параметры

*трустлвл*<br/>
По завершении этой операции уровень доверия класса среды выполнения, который `ActivationFactory` создает экземпляр.

### <a name="return-value"></a>Возвращаемое значение

S_OK в случае успеха; в противном случае выдается ошибка утверждения, а для *трустлвл* задается значение `FullTrust` .

## <a name="activationfactoryqueryinterface"></a><a name="queryinterface"></a> Метод ActivationFactory:: QueryInterface

Извлекает указатель на указанный интерфейс.

```cpp
STDMETHOD(
   QueryInterface
)(REFIID riid, _Deref_out_ void **ppvObject);
```

### <a name="parameters"></a>Параметры

*riid*<br/>
Идентификатор интерфейса.

*ппвобжект*<br/>
После завершения этой операции указатель на интерфейс, указанный параметром *riid*.

### <a name="return-value"></a>Возвращаемое значение

Значение S_OK, если операция завершилась успешно; в противном случае — значение HRESULT, описывающее тип сбоя.

## <a name="activationfactoryrelease"></a><a name="release"></a> Метод ActivationFactory:: Release

Уменьшает значение счетчика ссылок текущего `ActivationFactory` объекта.

```cpp
STDMETHOD_(
   ULONG,
   Release
)();
```

### <a name="return-value"></a>Возвращаемое значение

Значение S_OK, если операция завершилась успешно; в противном случае — значение HRESULT, описывающее тип сбоя.
