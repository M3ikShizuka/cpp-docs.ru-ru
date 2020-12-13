---
description: 'Дополнительные сведения о: Ккрсеап Class'
title: Класс Ккрсеап
ms.date: 11/04/2016
f1_keywords:
- CCRTHeap
- ATLMEM/ATL::CCRTHeap
- ATLMEM/ATL::CCRTHeap::Allocate
- ATLMEM/ATL::CCRTHeap::Free
- ATLMEM/ATL::CCRTHeap::GetSize
- ATLMEM/ATL::CCRTHeap::Reallocate
helpviewer_keywords:
- CCRTHeap class
ms.assetid: 321bd6c5-1856-4ff7-8590-95044a1209f7
ms.openlocfilehash: c256139f37a4b0caa0a60f1a87fd71b6a3a8de3b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97142016"
---
# <a name="ccrtheap-class"></a>Класс Ккрсеап

Этот класс реализует [иатлмеммгр](../../atl/reference/iatlmemmgr-class.md) с помощью функций кучи CRT.

## <a name="syntax"></a>Синтаксис

```
class CCRTHeap : public IAtlMemMgr
```

## <a name="members"></a>Члены

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Ккрсеап:: allocate](#allocate)|Вызовите этот метод, чтобы выделить блок памяти.|
|[Ккрсеап:: Free](#free)|Вызовите этот метод, чтобы освободить блок памяти, выделенный этим диспетчером памяти.|
|[Ккрсеап:: DataSize](#getsize)|Вызовите этот метод, чтобы получить выделенный размер блока памяти, выделенного этим диспетчером памяти.|
|[Ккрсеап:: перераспределение](#reallocate)|Вызовите этот метод для перераспределения памяти, выделенной данным диспетчером памяти.|

## <a name="remarks"></a>Комментарии

`CCRTHeap` реализует функции выделения памяти с помощью функций кучи CRT, включая [malloc](../../c-runtime-library/reference/malloc.md), [Free](../../c-runtime-library/reference/free.md), [Alloc](../../c-runtime-library/reference/realloc.md)и [_msize](../../c-runtime-library/reference/msize.md).

## <a name="example"></a>Пример

См. пример для [иатлмеммгр](../../atl/reference/iatlmemmgr-class.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`IAtlMemMgr`

`CCRTHeap`

## <a name="requirements"></a>Требования

**Заголовок:** атлмем. h

## <a name="ccrtheapallocate"></a><a name="allocate"></a> Ккрсеап:: allocate

Вызовите этот метод, чтобы выделить блок памяти.

```
virtual __declspec(allocator) void* Allocate(size_t nBytes) throw();
```

### <a name="parameters"></a>Параметры

*nBytes*<br/>
Запрошенное число байтов в новом блоке памяти.

### <a name="return-value"></a>Возвращаемое значение

Возвращает указатель на начало выделенного блока памяти.

### <a name="remarks"></a>Комментарии

Вызовите метод [ккрсеап:: Free](#free) или [ккрсеап:: reallocate](#reallocate) , чтобы освободить память, выделенную этим методом.

Реализуется с помощью [malloc](../../c-runtime-library/reference/malloc.md).

## <a name="ccrtheapfree"></a><a name="free"></a> Ккрсеап:: Free

Вызовите этот метод, чтобы освободить блок памяти, выделенный этим диспетчером памяти.

```
virtual void Free(void* p) throw();
```

### <a name="parameters"></a>Параметры

*p*<br/>
Указатель на область памяти, выделенную ранее данным диспетчером памяти. Значение NULL является допустимым и не выполняет никаких действий.

### <a name="remarks"></a>Комментарии

Реализовано с помощью [Free](../../c-runtime-library/reference/free.md).

## <a name="ccrtheapgetsize"></a><a name="getsize"></a> Ккрсеап:: DataSize

Вызовите этот метод, чтобы получить выделенный размер блока памяти, выделенного этим диспетчером памяти.

```
virtual size_t GetSize(void* p) throw();
```

### <a name="parameters"></a>Параметры

*p*<br/>
Указатель на область памяти, выделенную ранее данным диспетчером памяти.

### <a name="return-value"></a>Возвращаемое значение

Возвращает размер выделенного блока памяти в байтах.

### <a name="remarks"></a>Комментарии

Реализуется с помощью [_msize](../../c-runtime-library/reference/msize.md).

## <a name="ccrtheapreallocate"></a><a name="reallocate"></a> Ккрсеап:: перераспределение

Вызовите этот метод для перераспределения памяти, выделенной данным диспетчером памяти.

```
virtual __declspec(allocator) void* Reallocate(void* p, size_t nBytes) throw();
```

### <a name="parameters"></a>Параметры

*p*<br/>
Указатель на область памяти, выделенную ранее данным диспетчером памяти.

*nBytes*<br/>
Запрошенное число байтов в новом блоке памяти.

### <a name="return-value"></a>Возвращаемое значение

Возвращает указатель на начало выделенного блока памяти.

### <a name="remarks"></a>Комментарии

Вызовите метод [ккрсеап:: Free](#free) , чтобы освободить память, выделенную этим методом. Реализуется с помощью [перераспределения](../../c-runtime-library/reference/realloc.md).

## <a name="see-also"></a>См. также раздел

[Общие сведения о классах](../../atl/atl-class-overview.md)<br/>
[Класс Ккомхеап](../../atl/reference/ccomheap-class.md)<br/>
[Класс CWin32Heap](../../atl/reference/cwin32heap-class.md)<br/>
[Класс CLocalHeap](../../atl/reference/clocalheap-class.md)<br/>
[Класс CCRTHeap](../../atl/reference/cglobalheap-class.md)<br/>
[Класс Иатлмеммгр](../../atl/reference/iatlmemmgr-class.md)
