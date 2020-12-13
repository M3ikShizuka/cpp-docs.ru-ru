---
description: 'Дополнительные сведения о: структура метод runtimeclassbaset'
title: Структура RuntimeClassBaseT
ms.date: 10/03/2018
ms.topic: reference
f1_keywords:
- implements/Microsoft::WRL::Details::RuntimeClassBaseT
- implements/Microsoft::WRL::Details::RuntimeClassBaseT::AsIID
- implements/Microsoft::WRL::Details::RuntimeClassBaseT::GetImplementedIIDS
helpviewer_keywords:
- Microsoft::WRL::Details::RuntimeClassBaseT structure
- Microsoft::WRL::Details::RuntimeClassBaseT::AsIID method
- Microsoft::WRL::Details::RuntimeClassBaseT::GetImplementedIIDS method
ms.assetid: a62775fb-3359-4f45-9ff1-c07fa8da464b
ms.openlocfilehash: 48f03a5d54eba455b60646ed47c48e228f07863e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97135295"
---
# <a name="runtimeclassbaset-structure"></a>Структура RuntimeClassBaseT

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

## <a name="syntax"></a>Синтаксис

```cpp
template <unsigned int RuntimeClassTypeT>
friend struct Details::RuntimeClassBaseT;
```

### <a name="parameters"></a>Параметры

*рунтимекласстипет*<br/>
Поле флагов, задающее один или несколько перечислителей [RuntimeClassType](runtimeclasstype-enumeration.md) .

## <a name="remarks"></a>Комментарии

Предоставляет вспомогательные методы для операций `QueryInterface` и получения идентификаторов интерфейсов.

## <a name="members"></a>Элементы

### <a name="protected-methods"></a>Защищенные методы

Имя                                                         | Описание
------------------------------------------------------------ | -----------------------------------------------------------------------------
[Метод runtimeclassbaset:: AsIID](#asiid)                           | Извлекает указатель на указанный идентификатор интерфейса.
[Метод runtimeclassbaset:: GetImplementedIIDS](#getimplementediids) | Извлекает массив идентификаторов интерфейса, реализованных указанным типом.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`RuntimeClassBaseT`

## <a name="requirements"></a>Требования

**Заголовок:** Implements. h

**Пространство имен:** Microsoft:: WRL::D состояния

## <a name="runtimeclassbasetasiid"></a><a name="asiid"></a> Метод runtimeclassbaset:: AsIID

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

```cpp
template<typename T>
__forceinline static HRESULT AsIID(
   _In_ T* implements,
   REFIID riid,
   _Deref_out_ void **ppvObject
);
```

### <a name="parameters"></a>Параметры

*T*<br/>
Тип, реализующий идентификатор интерфейса, указанный параметром *riid*.

*внедрен*<br/>
Переменная типа, заданная параметром-шаблоном *T*.

*riid*<br/>
Извлекаемый идентификатор интерфейса.

*ппвобжект*<br/>
Если эта операция выполнена успешно, указатель на указатель на интерфейс, указанный параметром *riid*.

### <a name="return-value"></a>Возвращаемое значение

S_OK в случае успеха; в противном случае возвращается значение HRESULT, описывающее ошибку.

### <a name="remarks"></a>Комментарии

Извлекает указатель на указанный идентификатор интерфейса.

## <a name="runtimeclassbasetgetimplementediids"></a><a name="getimplementediids"></a> Метод runtimeclassbaset:: GetImplementedIIDS

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

```cpp
template<typename T>
__forceinline static HRESULT GetImplementedIIDS(
   _In_ T* implements,
   _Out_ ULONG *iidCount,
   _Deref_out_ _Deref_post_cap_(*iidCount) IID **iids
);
```

### <a name="parameters"></a>Параметры

*T*<br/>
Тип параметра *Implements* .

*внедрен*<br/>
Указатель на тип, заданный параметром *T*.

*iidCount*<br/>
Максимальное число идентификаторов интерфейсов для извлечения.

*идентификаторов IID*<br/>
Если эта операция завершается успешно, массив идентификаторов интерфейса, реализованный типом *T*.

### <a name="return-value"></a>Возвращаемое значение

S_OK в случае успеха; в противном случае возвращается значение HRESULT, описывающее ошибку.

### <a name="remarks"></a>Комментарии

Извлекает массив идентификаторов интерфейса, реализованных указанным типом.
