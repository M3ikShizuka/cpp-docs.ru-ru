---
description: 'Дополнительные сведения о: Ккрталлокатор Class'
title: Класс Ккрталлокатор
ms.date: 11/04/2016
f1_keywords:
- CCRTAllocator
- ATLCORE/ATL::CCRTAllocator
- ATLCORE/ATL::CCRTAllocator::Allocate
- ATLCORE/ATL::CCRTAllocator::Free
- ATLCORE/ATL::CCRTAllocator::Reallocate
helpviewer_keywords:
- CCRTAllocator class
ms.assetid: 3e1b8cb0-859a-41ab-8e93-6f0b5ceca49d
ms.openlocfilehash: 378a1c27a6c2dde9fbcb24eb9b51b64c3af7e8aa
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97142068"
---
# <a name="ccrtallocator-class"></a>Класс Ккрталлокатор

Этот класс предоставляет методы для управления памятью с помощью подпрограмм памяти CRT.

## <a name="syntax"></a>Синтаксис

```
class ATL::CCRTAllocator
```

## <a name="members"></a>Члены

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Ккрталлокатор:: allocate](#allocate)|Статически Вызовите этот метод, чтобы выделить память.|
|[Ккрталлокатор:: Free](#free)|Статически Вызовите этот метод, чтобы освободить память.|
|[Ккрталлокатор:: перераспределение](#reallocate)|Статически Вызовите этот метод, чтобы перераспределить память.|

## <a name="remarks"></a>Комментарии

Этот класс используется [чеапптр](../../atl/reference/cheapptr-class.md) для предоставления подпрограмм CRT для выделения памяти. Аналогичный класс [ккомаллокатор](../../atl/reference/ccomallocator-class.md)предоставляет те же методы, что и подпрограммы com.

## <a name="requirements"></a>Требования

**Заголовок:** атлкоре. h

## <a name="ccrtallocatorallocate"></a><a name="allocate"></a> Ккрталлокатор:: allocate

Вызовите эту статическую функция для выделения памяти.

```
static __declspec(allocator) void* Allocate(size_t nBytes) throw();
```

### <a name="parameters"></a>Параметры

*nBytes*<br/>
Количество байтов, которые необходимо выделить.

### <a name="return-value"></a>Возвращаемое значение

Возвращает указатель void на выделенное пространство или значение NULL, если памяти недостаточно.

### <a name="remarks"></a>Комментарии

Выделяет память. Дополнительные сведения см. в разделе [malloc](../../c-runtime-library/reference/malloc.md) .

## <a name="ccrtallocatorfree"></a><a name="free"></a> Ккрталлокатор:: Free

Вызовите эту статическую функцию, чтобы освободить память.

```
static void Free(void* p) throw();
```

### <a name="parameters"></a>Параметры

*p*<br/>
Указатель на выделенную область памяти.

### <a name="remarks"></a>Комментарии

Освобождает выделенную память. Дополнительные сведения см. в [бесплатном](../../c-runtime-library/reference/free.md) разделе.

## <a name="ccrtallocatorreallocate"></a><a name="reallocate"></a> Ккрталлокатор:: перераспределение

Вызовите эту статическую функцию для повторного выделения памяти.

```
static __declspec(allocator) void* Reallocate(void* p, size_t nBytes) throw();
```

### <a name="parameters"></a>Параметры

*p*<br/>
Указатель на выделенную область памяти.

*nBytes*<br/>
Количество байтов, которые необходимо выделить повторно.

### <a name="return-value"></a>Возвращаемое значение

Возвращает указатель void на выделенное пространство или значение NULL, если памяти недостаточно.

### <a name="remarks"></a>Комментарии

Изменяет объем выделенной памяти. Дополнительные сведения см. в разделе [перераспределить](../../c-runtime-library/reference/realloc.md) .

## <a name="see-also"></a>См. также раздел

[Класс Чеапптр](../../atl/reference/cheapptr-class.md)<br/>
[Класс Ккомаллокатор](../../atl/reference/ccomallocator-class.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
