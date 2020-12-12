---
description: 'Дополнительные сведения о: структура InvokeHelper'
title: InvokeHelper - структура
ms.date: 10/18/2018
ms.topic: reference
f1_keywords:
- event/Microsoft::WRL::Details::InvokeHelper
- event/Microsoft::WRL::Details::InvokeHelper::callback_
- event/Microsoft::WRL::Details::InvokeHelper::Invoke
- event/Microsoft::WRL::Details::InvokeHelper::InvokeHelper
helpviewer_keywords:
- Microsoft::WRL::Details::InvokeHelper structure
- Microsoft::WRL::Details::callback_ data member
- Microsoft::WRL::Details::Invoke method
- Microsoft::WRL::Details::InvokeHelper, constructor
ms.assetid: 555ad2bc-4dd6-4e65-a2e2-1242c395f0e5
ms.openlocfilehash: 0b9bb8abb59cce5a3c25d795d0946ffbe88d0076
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97299024"
---
# <a name="invokehelper-structure"></a>InvokeHelper - структура

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

## <a name="syntax"></a>Синтаксис

```cpp
template<typename TDelegateInterface, typename TCallback, unsigned int argCount>
struct InvokeHelper;

template<typename TDelegateInterface, typename TCallback>
struct InvokeHelper<TDelegateInterface, TCallback, 0> :
    public Microsoft::WRL::RuntimeClass<
        RuntimeClassFlags<Delegate>,
        TDelegateInterface
    >;

template<typename TDelegateInterface, typename TCallback>
struct InvokeHelper<TDelegateInterface, TCallback, 1> :
    public Microsoft::WRL::RuntimeClass<
        RuntimeClassFlags<Delegate>,
        TDelegateInterface
    >;

template<typename TDelegateInterface, typename TCallback>
struct InvokeHelper<TDelegateInterface, TCallback, 2> :
    public Microsoft::WRL::RuntimeClass<
        RuntimeClassFlags<Delegate>,
        TDelegateInterface
    >;

template<typename TDelegateInterface, typename TCallback>
struct InvokeHelper<TDelegateInterface, TCallback, 3> :
    public Microsoft::WRL::RuntimeClass<
        RuntimeClassFlags<Delegate>,
        TDelegateInterface
    >;

template<typename TDelegateInterface, typename TCallback>
struct InvokeHelper<TDelegateInterface, TCallback, 4> :
    Microsoft::WRL::RuntimeClass<
        RuntimeClassFlags<Delegate>,
        TDelegateInterface
    >;

template<typename TDelegateInterface, typename TCallback>
struct InvokeHelper<TDelegateInterface, TCallback, 5> :
    Microsoft::WRL::RuntimeClass<
        RuntimeClassFlags<Delegate>,
        TDelegateInterface
    >;

template<typename TDelegateInterface, typename TCallback>
struct InvokeHelper<TDelegateInterface, TCallback, 6> :
    Microsoft::WRL::RuntimeClass<
        RuntimeClassFlags<Delegate>,
        TDelegateInterface
    >;

template<typename TDelegateInterface, typename TCallback>
struct InvokeHelper<TDelegateInterface, TCallback, 7> :
    Microsoft::WRL::RuntimeClass<
        RuntimeClassFlags<Delegate>,
        TDelegateInterface
    >;

template<typename TDelegateInterface, typename TCallback>
struct InvokeHelper<TDelegateInterface, TCallback, 8> :
    Microsoft::WRL::RuntimeClass<
        RuntimeClassFlags<Delegate>,
        TDelegateInterface
    >;

template<typename TDelegateInterface, typename TCallback>
struct InvokeHelper<TDelegateInterface, TCallback, 9> :
    Microsoft::WRL::RuntimeClass<
        RuntimeClassFlags<Delegate>,
        TDelegateInterface
    >;
```

### <a name="parameters"></a>Параметры

*тделегатеинтерфаце*<br/>
Тип интерфейса делегата.

*ткаллбакк*<br/>
Тип функции обработчика событий.

*аргкаунт*<br/>
Число аргументов в `InvokeHelper` специализации.

## <a name="remarks"></a>Комментарии

Предоставляет реализацию `Invoke()` метода на основе указанного числа и типа аргументов.

## <a name="members"></a>Элементы

### <a name="public-typedefs"></a>Общедоступные определения типов

Имя     | Описание
-------- | -----------------------------------------------------------------------------
`Traits` | Синоним класса, определяющий тип каждого аргумента обработчика событий.

### <a name="public-constructors"></a>Открытые конструкторы

name                                        | Описание
------------------------------------------- | -------------------------------------------------------
[InvokeHelper:: InvokeHelper](#invokehelper) | Инициализирует новый экземпляр класса `InvokeHelper`.

### <a name="public-methods"></a>Открытые методы

name                            | Описание
------------------------------- | -----------------------------------------------------------------------------------
[InvokeHelper:: Invoke](#invoke) | Вызывает обработчик событий, сигнатура которого содержит указанное число аргументов.

### <a name="public-data-members"></a>Открытые члены данных

Имя                                 | Описание
------------------------------------ | ----------------------------------------------------------
[InvokeHelper:: callback_](#callback) | Представляет обработчик событий, вызываемый при возникновении события.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`InvokeHelper`

## <a name="requirements"></a>Требования

**Заголовок:** Event. h

**Пространство имен:** Microsoft:: WRL::D состояния

## <a name="invokehelpercallback_"></a><a name="callback"></a> InvokeHelper:: callback_

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

```cpp
TCallback callback_;
```

### <a name="remarks"></a>Комментарии

Представляет обработчик событий, вызываемый при возникновении события.

`TCallback`Параметр шаблона задает тип обработчика событий.

## <a name="invokehelperinvoke"></a><a name="invoke"></a> InvokeHelper:: Invoke

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

```cpp
STDMETHOD(
   Invoke
)();
STDMETHOD(
   Invoke
)(typename Traits;
STDMETHOD(
   Invoke
)( typename Traits;
STDMETHOD(
   Invoke
)( typename Traits;
STDMETHOD(
   Invoke
)( typename Traits;
STDMETHOD(
   Invoke
)( typename Traits;
STDMETHOD(
   Invoke
)( typename Traits;
STDMETHOD(
   Invoke
)( typename Traits;
STDMETHOD(
   Invoke
)( typename Traits;
STDMETHOD(
   Invoke
)( typename Traits;
```

### <a name="parameters"></a>Параметры

*arg1*<br/>
Аргумент 1.

*arg2*<br/>
Аргумент 2.

*arg3*<br/>
Аргумент 3.

*arg4*<br/>
Аргумент 4.

*arg5*<br/>
Аргумент 5.

*arg6*<br/>
Аргумент 6.

*arg7*<br/>
Аргумент 7.

*arg8*<br/>
Аргумент 8.

*arg9*<br/>
Аргумент 9.

### <a name="return-value"></a>Возвращаемое значение

S_OK в случае успеха; в противном случае возвращается значение HRESULT, описывающее ошибку.

### <a name="remarks"></a>Комментарии

Вызывает обработчик событий, сигнатура которого содержит указанное число аргументов.

## <a name="invokehelperinvokehelper"></a><a name="invokehelper"></a> InvokeHelper:: InvokeHelper

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

```cpp
explicit InvokeHelper(
   TCallback callback
);
```

### <a name="parameters"></a>Параметры

*обратный вызов*<br/>
Обработчик событий.

### <a name="remarks"></a>Комментарии

Инициализирует новый экземпляр класса `InvokeHelper`.

`TCallback`Параметр шаблона задает тип обработчика событий.
