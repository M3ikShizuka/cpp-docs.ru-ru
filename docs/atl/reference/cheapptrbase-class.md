---
description: 'Дополнительные сведения о: Чеапптрбасе Class'
title: Класс Чеапптрбасе
ms.date: 11/04/2016
f1_keywords:
- CHeapPtrBase
- ATLCORE/ATL::CHeapPtrBase
- ATLCORE/ATL::CHeapPtrBase::AllocateBytes
- ATLCORE/ATL::CHeapPtrBase::Attach
- ATLCORE/ATL::CHeapPtrBase::Detach
- ATLCORE/ATL::CHeapPtrBase::Free
- ATLCORE/ATL::CHeapPtrBase::ReallocateBytes
- ATLCORE/ATL::CHeapPtrBase::m_pData
helpviewer_keywords:
- CHeapPtrBase class
ms.assetid: 501ac1b2-fb34-4c72-b7e6-a4f1fc8fda21
ms.openlocfilehash: 6186f68066f4c159c16c458f9f00725478aa98a0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97141639"
---
# <a name="cheapptrbase-class"></a>Класс Чеапптрбасе

Этот класс образует базу для нескольких классов указателей смарт-кучи.

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```
template <class T, class Allocator = CCRTAllocator>
class CHeapPtrBase
```

#### <a name="parameters"></a>Параметры

*T*<br/>
Тип объекта, сохраняемый в куче.

*Выделен*<br/>
Используемый класс выделения памяти. По умолчанию подпрограммы CRT используются для выделения и освобождения памяти.

## <a name="members"></a>Элементы

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Чеапптрбасе:: ~ Чеапптрбасе](#dtor)|Деструктор|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Чеапптрбасе:: Аллокатебитес](#allocatebytes)|Вызовите этот метод, чтобы выделить память.|
|[Чеапптрбасе:: Attach](#attach)|Вызовите этот метод, чтобы стать владельцем существующего указателя.|
|[Чеапптрбасе::D етач](#detach)|Вызовите этот метод, чтобы освободить владение указателем.|
|[Чеапптрбасе:: Free](#free)|Вызовите этот метод, чтобы удалить объект, на который указывает `CHeapPtrBase` .|
|[Чеапптрбасе:: Реаллокатебитес](#reallocatebytes)|Вызовите этот метод, чтобы перераспределить память.|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[Чеапптрбасе:: operator T *](#operator_t_star)|Оператор CAST.|
|[Чеапптрбасе:: operator &](#operator_amp)|Оператора &.|
|[Чеапптрбасе:: operator — >](#operator_ptr)|Оператор указателя на член.|

### <a name="public-data-members"></a>Открытые члены данных

|Имя|Описание|
|----------|-----------------|
|[Чеапптрбасе:: m_pData](#m_pdata)|Переменная члена данных указателя.|

## <a name="remarks"></a>Комментарии

Этот класс образует базу для нескольких классов указателей смарт-кучи. Производные классы, например [чеапптр](../../atl/reference/cheapptr-class.md) и [ккомхеапптр](../../atl/reference/ccomheapptr-class.md), добавляют собственные конструкторы и операторы. Примеры реализации см. в этих классах.

## <a name="requirements"></a>Требования

**Заголовок:** атлкоре. h

## <a name="cheapptrbaseallocatebytes"></a><a name="allocatebytes"></a> Чеапптрбасе:: Аллокатебитес

Вызовите этот метод, чтобы выделить память.

```
bool AllocateBytes(size_t nBytes) throw();
```

### <a name="parameters"></a>Параметры

*nBytes*<br/>
Число байтов памяти для выделения.

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение true, если память успешно выделена, и false в противном случае.

### <a name="remarks"></a>Комментарии

В отладочных сборках произойдет сбой утверждения, если переменная члена [чеапптрбасе:: m_pData](#m_pdata) указывает на существующее значение. то есть он не равен NULL.

## <a name="cheapptrbaseattach"></a><a name="attach"></a> Чеапптрбасе:: Attach

Вызовите этот метод, чтобы стать владельцем существующего указателя.

```cpp
void Attach(T* pData) throw();
```

### <a name="parameters"></a>Параметры

*pData*<br/>
`CHeapPtrBase`Объект будет становиться владельцем этого указателя.

### <a name="remarks"></a>Комментарии

Когда `CHeapPtrBase` объект получает владение указателем, он автоматически удаляет указатель и все выделенные данные, когда оно выходит за пределы области.

В отладочных сборках произойдет сбой утверждения, если переменная члена [чеапптрбасе:: m_pData](#m_pdata) указывает на существующее значение. то есть он не равен NULL.

## <a name="cheapptrbasecheapptrbase"></a><a name="dtor"></a> Чеапптрбасе:: ~ Чеапптрбасе

Деструктор

```
~CHeapPtrBase() throw();
```

### <a name="remarks"></a>Комментарии

Освобождает все выделенные ресурсы.

## <a name="cheapptrbasedetach"></a><a name="detach"></a> Чеапптрбасе::D етач

Вызовите этот метод, чтобы освободить владение указателем.

```
T* Detach() throw();
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает копию указателя.

### <a name="remarks"></a>Комментарии

Освобождает владение указателем, устанавливает для переменной-члена [чеапптрбасе:: m_pData](#m_pdata) значение NULL и возвращает копию указателя.

## <a name="cheapptrbasefree"></a><a name="free"></a> Чеапптрбасе:: Free

Вызовите этот метод, чтобы удалить объект, на который указывает `CHeapPtrBase` .

```cpp
void Free() throw();
```

### <a name="remarks"></a>Комментарии

Объект, на который указывает, `CHeapPtrBase` освобождается, и переменной-члену [чеапптрбасе:: m_pData](#m_pdata) присваивается значение null.

## <a name="cheapptrbasem_pdata"></a><a name="m_pdata"></a> Чеапптрбасе:: m_pData

Переменная члена данных указателя.

```
T* m_pData;
```

### <a name="remarks"></a>Комментарии

Эта переменная члена содержит сведения об указателе.

## <a name="cheapptrbaseoperator-amp"></a><a name="operator_amp"></a> Чеапптрбасе:: operator &amp;

Оператора &.

```
T** operator&() throw();
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает адрес объекта, на который указывает `CHeapPtrBase` объект.

## <a name="cheapptrbaseoperator--gt"></a><a name="operator_ptr"></a> Чеапптрбасе:: operator —&gt;

Оператор указателя на член.

```
T* operator->() const throw();
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение переменной члена [чеапптрбасе:: m_pData](#m_pdata) .

### <a name="remarks"></a>Комментарии

Этот оператор используется для вызова метода в классе, на который указывает `CHeapPtrBase` объект. В отладочных сборках произойдет сбой утверждения, если `CHeapPtrBase` указывает на значение null.

## <a name="cheapptrbaseoperator-t"></a><a name="operator_t_star"></a> Чеапптрбасе:: operator T *

Оператор CAST.

```
operator T*() const throw();
```

### <a name="remarks"></a>Комментарии

Возвращает [чеапптрбасе:: m_pData](#m_pdata).

## <a name="cheapptrbasereallocatebytes"></a><a name="reallocatebytes"></a> Чеапптрбасе:: Реаллокатебитес

Вызовите этот метод, чтобы перераспределить память.

```
bool ReallocateBytes(size_t nBytes) throw();
```

### <a name="parameters"></a>Параметры

*nBytes*<br/>
Новый объем памяти, выделяемый в байтах.

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение true, если память успешно выделена, и false в противном случае.

## <a name="see-also"></a>См. также раздел

[Класс Чеапптр](../../atl/reference/cheapptr-class.md)<br/>
[Класс Ккомхеапптр](../../atl/reference/ccomheapptr-class.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
