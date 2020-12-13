---
description: 'Дополнительные сведения о: Ккомаллокатор Class'
title: Класс Ккомаллокатор
ms.date: 11/04/2016
f1_keywords:
- CComAllocator
- ATLBASE/ATL::CComAllocator
- ATLBASE/ATL::CComAllocator::Allocate
- ATLBASE/ATL::CComAllocator::Free
- ATLBASE/ATL::CComAllocator::Reallocate
helpviewer_keywords:
- CComAllocator class
ms.assetid: 0cd706fd-0c7b-42d3-9054-febe2966fc8e
ms.openlocfilehash: 886692f6a55ac096e51fd6888f941d63bf089263
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97146956"
---
# <a name="ccomallocator-class"></a>Класс Ккомаллокатор

Этот класс предоставляет методы для управления памятью с помощью подпрограмм COM-памяти.

## <a name="syntax"></a>Синтаксис

```
class CComAllocator
```

## <a name="members"></a>Члены

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Ккомаллокатор:: allocate](#allocate)|Вызовите этот статический метод, чтобы выделить память.|
|[Ккомаллокатор:: Free](#free)|Вызовите этот статический метод, чтобы освободить выделенную память.|
|[Ккомаллокатор:: перераспределение](#reallocate)|Вызовите этот статический метод, чтобы перераспределить память.|

## <a name="remarks"></a>Комментарии

Этот класс используется [ккомхеапптр](../../atl/reference/ccomheapptr-class.md) для предоставления подпрограмм выделения памяти com. Аналогичный класс [ккрталлокатор](../../atl/reference/ccrtallocator-class.md)предоставляет те же методы, что и подпрограммы CRT.

## <a name="requirements"></a>Требования

**Заголовок:** atlbase. h

## <a name="ccomallocatorallocate"></a><a name="allocate"></a> Ккомаллокатор:: allocate

Вызовите эту статическую функция для выделения памяти.

```
static void* Allocate(size_t nBytes) throw();
```

### <a name="parameters"></a>Параметры

*nBytes*<br/>
Количество байтов, которые необходимо выделить.

### <a name="return-value"></a>Возвращаемое значение

Возвращает указатель void на выделенное пространство или значение NULL, если памяти недостаточно.

### <a name="remarks"></a>Комментарии

Выделяет память. Дополнительные сведения см. в разделе [CoTaskMemAlloc](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) .

## <a name="ccomallocatorfree"></a><a name="free"></a> Ккомаллокатор:: Free

Вызовите эту статическую функцию, чтобы освободить выделенную память.

```
static void Free(void* p) throw();
```

### <a name="parameters"></a>Параметры

*p*<br/>
Указатель на выделенную область памяти.

### <a name="remarks"></a>Комментарии

Освобождает выделенную память. Дополнительные сведения см. в разделе [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) .

## <a name="ccomallocatorreallocate"></a><a name="reallocate"></a> Ккомаллокатор:: перераспределение

Вызовите эту статическую функцию для повторного выделения памяти.

```
static void* Reallocate(void* p, size_t nBytes) throw();
```

### <a name="parameters"></a>Параметры

*p*<br/>
Указатель на выделенную область памяти.

*nBytes*<br/>
Количество байтов, которые необходимо выделить повторно.

### <a name="return-value"></a>Возвращаемое значение

Возвращает указатель типа void на выделенное пространство или значение NULL, если недостаточно памяти

### <a name="remarks"></a>Комментарии

Изменяет объем выделенной памяти. Дополнительные сведения см. в разделе [котаскмемреаллок](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemrealloc) .

## <a name="see-also"></a>См. также раздел

[Класс Ккомхеапптр](../../atl/reference/ccomheapptr-class.md)<br/>
[Класс Ккрталлокатор](../../atl/reference/ccrtallocator-class.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
