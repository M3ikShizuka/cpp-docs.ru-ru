---
description: 'Дополнительные сведения о: CCRTHeap Class'
title: Класс CCRTHeap
ms.date: 11/04/2016
f1_keywords:
- CGlobalHeap
- ATLMEM/ATL::CGlobalHeap
- ATLMEM/ATL::CGlobalHeap::Allocate
- ATLMEM/ATL::CGlobalHeap::Free
- ATLMEM/ATL::CGlobalHeap::GetSize
- ATLMEM/ATL::CGlobalHeap::Reallocate
helpviewer_keywords:
- CGlobalHeap class
ms.assetid: e348d838-3aa7-4bee-a1b3-cd000c99f834
ms.openlocfilehash: 349dd2155bdc68024171c07e48c648bae2b6aa7e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97141691"
---
# <a name="cglobalheap-class"></a>Класс CCRTHeap

Этот класс реализует [иатлмеммгр](../../atl/reference/iatlmemmgr-class.md) с помощью глобальных функций кучи Win32.

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```
class CGlobalHeap : public IAtlMemMgr
```

## <a name="members"></a>Члены

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CCRTHeap:: allocate](#allocate)|Вызовите этот метод, чтобы выделить блок памяти.|
|[CCRTHeap:: Free](#free)|Вызовите этот метод, чтобы освободить блок памяти, выделенный этим диспетчером памяти.|
|[CCRTHeap:: DataSize](#getsize)|Вызовите этот метод, чтобы получить выделенный размер блока памяти, выделенного этим диспетчером памяти.|
|[CCRTHeap:: перераспределение](#reallocate)|Вызовите этот метод для перераспределения памяти, выделенной данным диспетчером памяти.|

## <a name="remarks"></a>Комментарии

`CGlobalHeap` реализует функции выделения памяти с помощью глобальных функций кучи Win32.

> [!NOTE]
> Глобальные функции кучи выполняются медленнее, чем другие функции управления памятью, и не предоставляют столько функций. Поэтому новые приложения должны использовать [функции кучи](/windows/win32/Memory/heap-functions). Они доступны в классе [CWin32Heap](../../atl/reference/cwin32heap-class.md) . Глобальные функции по-прежнему используются в DDE и функциях буфера обмена.

## <a name="example"></a>Пример

См. пример для [иатлмеммгр](../../atl/reference/iatlmemmgr-class.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`IAtlMemMgr`

`CGlobalHeap`

## <a name="requirements"></a>Требования

**Заголовок:** атлмем. h

## <a name="cglobalheapallocate"></a><a name="allocate"></a> CCRTHeap:: allocate

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

Вызовите метод [CCRTHeap:: Free](#free) или [CCRTHeap:: reallocate](#reallocate) , чтобы освободить память, выделенную этим методом.

Реализуется с помощью [GlobalAlloc](/windows/win32/api/winbase/nf-winbase-globalalloc) с параметром Flag GMEM_FIXED.

## <a name="cglobalheapfree"></a><a name="free"></a> CCRTHeap:: Free

Вызовите этот метод, чтобы освободить блок памяти, выделенный этим диспетчером памяти.

```
virtual void Free(void* p) throw();
```

### <a name="parameters"></a>Параметры

*p*<br/>
Указатель на область памяти, выделенную ранее данным диспетчером памяти. Значение NULL является допустимым и не выполняет никаких действий.

### <a name="remarks"></a>Комментарии

Реализуется с помощью [GlobalFree](/windows/win32/api/winbase/nf-winbase-globalfree).

## <a name="cglobalheapgetsize"></a><a name="getsize"></a> CCRTHeap:: DataSize

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

Реализуется с помощью [глобалсизе](/windows/win32/api/winbase/nf-winbase-globalsize).

## <a name="cglobalheapreallocate"></a><a name="reallocate"></a> CCRTHeap:: перераспределение

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

Вызовите метод [CCRTHeap:: Free](#free) , чтобы освободить память, выделенную этим методом.

Реализуется с помощью [LocalLock](/windows/win32/api/winbase/nf-winbase-globalrealloc).

## <a name="see-also"></a>См. также раздел

[Общие сведения о классах](../../atl/atl-class-overview.md)<br/>
[Класс Ккомхеап](../../atl/reference/ccomheap-class.md)<br/>
[Класс CWin32Heap](../../atl/reference/cwin32heap-class.md)<br/>
[Класс CLocalHeap](../../atl/reference/clocalheap-class.md)<br/>
[Класс Ккрсеап](../../atl/reference/ccrtheap-class.md)<br/>
[Класс Иатлмеммгр](../../atl/reference/iatlmemmgr-class.md)
