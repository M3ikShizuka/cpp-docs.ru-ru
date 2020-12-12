---
description: 'Дополнительные сведения о: оператор comptrrefbase Class'
title: ComPtrRefBase - класс
ms.date: 10/03/2018
ms.topic: reference
f1_keywords:
- client/Microsoft::WRL::Details::ComPtrRefBase
- client/Microsoft::WRL::Details::ComPtrRefBase::operator IInspectable**
- client/Microsoft::WRL::Details::ComPtrRefBase::operator IUnknown**
- client/Microsoft::WRL::Details::ComPtrRefBase::ptr_
helpviewer_keywords:
- Microsoft::WRL::Details::ComPtrRefBase class
- Microsoft::WRL::Details::ComPtrRefBase::operator IInspectable** operator
- Microsoft::WRL::Details::ComPtrRefBase::operator IUnknown** operator
- Microsoft::WRL::Details::ComPtrRefBase::ptr_ data member
ms.assetid: 6d344c1a-cc13-4a3f-8a0d-f167ccb9348f
ms.openlocfilehash: 4dce58e8292092084916c24153d543f2a45856fa
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97273141"
---
# <a name="comptrrefbase-class"></a>ComPtrRefBase - класс

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

## <a name="syntax"></a>Синтаксис

```cpp
template <typename T>
class ComPtrRefBase;
```

### <a name="parameters"></a>Параметры

*T*<br/>
Тип [ComPtr \<T> ](comptr-class.md) или производный от него тип, а не просто интерфейс, представленный `ComPtr` .

## <a name="remarks"></a>Комментарии

Представляет базовый класс для класса [ComPtrRef](comptrref-class.md) .

## <a name="members"></a>Элементы

### <a name="public-typedefs"></a>Общедоступные определения типов

Имя            | Описание
--------------- | -------------------------------------------------
`InterfaceType` | Синоним для типа параметра-шаблона *T*.

### <a name="public-operators"></a>Открытые операторы

Имя                                                                       | Описание
-------------------------------------------------------------------------- | -----------------------------------------------------------------------------------------------------
[Оператор comptrrefbase:: operator IInspectable * *](#operator-iinspectable-star-star) | Приводит текущий элемент данных [ptr_](#ptr) к интерфейсу с указателем на указатель `IInspectable` .
[Оператор comptrrefbase:: operator IUnknown * *](#operator-iunknown-star-star)         | Приводит текущий элемент данных [ptr_](#ptr) к интерфейсу с указателем на указатель `IUnknown` .

### <a name="protected-data-members"></a>Защищенные члены данных

Имя                        | Описание
--------------------------- | ----------------------------------------------------------------
[Оператор comptrrefbase::p tr_](#ptr) | Указатель на тип, заданный текущим параметром шаблона.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`ComPtrRefBase`

## <a name="requirements"></a>Требования

**Заголовок:** client.h

**Пространство имен:** Microsoft:: WRL::D состояния

## <a name="comptrrefbaseoperator-iinspectable-operator"></a><a name="operator-iinspectable-star-star"></a>Оператор оператор comptrrefbase:: operator IInspectable \* \*

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

```cpp
operator IInspectable**() const;
```

### <a name="remarks"></a>Комментарии

Приводит текущий элемент данных [ptr_](#ptr) к интерфейсу с указателем на указатель `IInspectable` .

Если текущий объект `ComPtrRefBase` не является производным от, генерируется ошибка `IInspectable` .

Это приведение доступно, только если `__WRL_CLASSIC_COM__` определено.

## <a name="comptrrefbaseoperator-iunknown-operator"></a><a name="operator-iunknown-star-star"></a> Оператор оператор comptrrefbase:: operator IUnknown * *

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

```cpp
operator IUnknown**() const;
```

### <a name="remarks"></a>Комментарии

Приводит текущий элемент данных [ptr_](#ptr) к интерфейсу с указателем на указатель `IUnknown` .

Если текущий объект `ComPtrRefBase` не является производным от, генерируется ошибка `IUnknown` .

## <a name="comptrrefbaseptr_"></a><a name="ptr"></a> Оператор comptrrefbase::p tr_

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

```cpp
T* ptr_;
```

### <a name="remarks"></a>Комментарии

Указатель на тип, заданный текущим параметром шаблона. `ptr_` защищенный элемент данных.
