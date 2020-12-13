---
description: 'Дополнительные сведения о: Чеапптр Class'
title: Класс Чеапптр
ms.date: 11/04/2016
f1_keywords:
- CHeapPtr
- ATLCORE/ATL::CHeapPtr
- ATLCORE/ATL::CHeapPtr::CHeapPtr
- ATLCORE/ATL::CHeapPtr::Allocate
- ATLCORE/ATL::CHeapPtr::Reallocate
helpviewer_keywords:
- CHeapPtr class
ms.assetid: e5c5bfd4-9bf1-4164-8a83-8155fe253454
ms.openlocfilehash: dc795c199562fa423a160b053c96983651d0812d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97141652"
---
# <a name="cheapptr-class"></a>Класс Чеапптр

Класс интеллектуального указателя для управления указателями кучи.

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```
template<typename T, class Allocator=CCRTAllocator>
class CHeapPtr : public CHeapPtrBase<T, Allocator>
```

#### <a name="parameters"></a>Параметры

*T*<br/>
Тип объекта, сохраняемый в куче.

*Выделен*<br/>
Используемый класс выделения памяти.

## <a name="members"></a>Элементы

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Чеапптр:: Чеапптр](#cheapptr)|Конструктор.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Чеапптр:: allocate](#allocate)|Вызовите этот метод, чтобы выделить память в куче для хранения объектов.|
|[Чеапптр:: перераспределение](#reallocate)|Вызовите этот метод, чтобы перераспределить память в куче.|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[Чеапптр:: operator =](#operator_eq)|Оператор присваивания.|

## <a name="remarks"></a>Комментарии

`CHeapPtr` является производным от [чеапптрбасе](../../atl/reference/cheapptrbase-class.md) и по умолчанию использует подпрограммы CRT (в [ккрталлокатор](../../atl/reference/ccrtallocator-class.md)) для выделения и освобождения памяти. Класс [чеапптрлист](../../atl/reference/cheapptrlist-class.md) может использоваться для создания списка указателей на кучу. См. также [ккомхеапптр](../../atl/reference/ccomheapptr-class.md), который использует подпрограммы выделения памяти com.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[чеапптрбасе](../../atl/reference/cheapptrbase-class.md)

`CHeapPtr`

## <a name="requirements"></a>Требования

**Заголовок:** атлкоре. h

## <a name="cheapptrallocate"></a><a name="allocate"></a> Чеапптр:: allocate

Вызовите этот метод, чтобы выделить память в куче для хранения объектов.

```
bool Allocate(size_t nElements = 1) throw();
```

### <a name="parameters"></a>Параметры

*нелементс*<br/>
Количество элементов, использованных для вычисления объема выделяемой памяти. Значение по умолчанию — 1.

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение true, если память была успешно выделена, и false в случае сбоя.

### <a name="remarks"></a>Комментарии

Подпрограммы распределителя используются для резервирования достаточного объема памяти в куче для хранения объектов *нелемент* типа, определенного в конструкторе.

### <a name="example"></a>Пример

[!code-cpp[NVC_ATL_Utilities#77](../../atl/codesnippet/cpp/cheapptr-class_1.cpp)]

## <a name="cheapptrcheapptr"></a><a name="cheapptr"></a> Чеапптр:: Чеапптр

Конструктор.

```
CHeapPtr() throw();
explicit CHeapPtr(T* p) throw();
CHeapPtr(CHeapPtr<T, Allocator>& p) throw();
```

### <a name="parameters"></a>Параметры

*p*<br/>
Существующий указатель кучи или `CHeapPtr` .

### <a name="remarks"></a>Комментарии

При необходимости можно создать указатель кучи с помощью существующего указателя или `CHeapPtr` объекта. В этом случае новый `CHeapPtr` объект несет ответственность за управление новым указателем и ресурсами.

### <a name="example"></a>Пример

[!code-cpp[NVC_ATL_Utilities#78](../../atl/codesnippet/cpp/cheapptr-class_2.cpp)]

## <a name="cheapptroperator-"></a><a name="operator_eq"></a> Чеапптр:: operator =

Оператор присвоения.

```
CHeapPtr<T, Allocator>& operator=(
    CHeapPtr<T, Allocator>& p) throw();
```

### <a name="parameters"></a>Параметры

*p*<br/>
Существующий объект `CHeapPtr`.

### <a name="return-value"></a>Возвращаемое значение

Возвращает ссылку на обновленную `CHeapPtr` .

### <a name="example"></a>Пример

[!code-cpp[NVC_ATL_Utilities#80](../../atl/codesnippet/cpp/cheapptr-class_3.cpp)]

## <a name="cheapptrreallocate"></a><a name="reallocate"></a> Чеапптр:: перераспределение

Вызовите этот метод, чтобы перераспределить память в куче.

```
bool Reallocate(size_t nElements) throw();
```

### <a name="parameters"></a>Параметры

*нелементс*<br/>
Новое число элементов, используемое для вычисления объема выделяемой памяти.

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение true, если память была успешно выделена, и false в случае сбоя.

### <a name="example"></a>Пример

[!code-cpp[NVC_ATL_Utilities#79](../../atl/codesnippet/cpp/cheapptr-class_4.cpp)]

## <a name="see-also"></a>См. также раздел

[Класс Чеапптрбасе](../../atl/reference/cheapptrbase-class.md)<br/>
[Класс Ккрталлокатор](../../atl/reference/ccrtallocator-class.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
