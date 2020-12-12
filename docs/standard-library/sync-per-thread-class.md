---
description: 'Дополнительные сведения о: sync_per_thread классе'
title: Класс sync_per_thread
ms.date: 11/04/2016
f1_keywords:
- allocators/stdext::sync_per_thread
- allocators/stdext::sync_per_thread::allocate
- allocators/stdext::sync_per_thread::deallocate
- allocators/stdext::sync_per_thread::equals
helpviewer_keywords:
- stdext::sync_per_thread
- stdext::sync_per_thread [C++], allocate
- stdext::sync_per_thread [C++], deallocate
- stdext::sync_per_thread [C++], equals
ms.assetid: 47bf75f8-5b02-4760-b1d3-3099d08fe14c
ms.openlocfilehash: dbce0441e32c97907bdf2cc5831a94c9af125453
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97183299"
---
# <a name="sync_per_thread-class"></a>Класс sync_per_thread

Описывает [фильтр синхронизации](../standard-library/allocators-header.md) , который предоставляет отдельный объект кэша для каждого потока.

## <a name="syntax"></a>Синтаксис

```cpp
template <class Cache>
class sync_per_thread
```

### <a name="parameters"></a>Параметры

*Мбайта*\
Тип кэша, связанный с фильтром синхронизации. Это может быть [`cache_chunklist`](../standard-library/cache-chunklist-class.md) , [`cache_freelist`](../standard-library/cache-freelist-class.md) или [`cache_suballoc`](../standard-library/cache-suballoc-class.md) .

## <a name="remarks"></a>Комментарии

Распределители, использующие `sync_per_thread`, могут быть равны несмотря на то, что блоки, выделенные в одном потоке, невозможно освободить из другого потока. При использовании одного из этих распределителей блоки памяти, выделенные в одном потоке, не должны быть видимы другим потокам. На практике это означает, что доступ к контейнеру, использующему один из этих распределителей, должен осуществляться только одним потоком.

### <a name="member-functions"></a>Функции элементов

|Функция-член|Описание|
|-|-|
|[памяти](#allocate)|Выделяет блок памяти.|
|[deallocate](#deallocate)|Освобождает указанное число объектов из памяти, начиная с заданной позиции.|
|[equals](#equals)|Сравнивает два кэша на равенство.|

## <a name="requirements"></a>Требования

**Заголовок:**\<allocators>

**Пространство имен:** stdext

## <a name="sync_per_threadallocate"></a><a name="allocate"></a> sync_per_thread:: allocate

Выделяет блок памяти.

```cpp
void *allocate(std::size_t count);
```

### <a name="parameters"></a>Параметры

*расчета*\
Число выделяемых элементов в массиве.

### <a name="remarks"></a>Комментарии

Функция-член возвращает результат вызова `cache::allocate(count)` в объекте кэша, который относится к текущему потоку. Если объект кэша для текущего потока не выделен, сначала такой объект будет выделен.

## <a name="sync_per_threaddeallocate"></a><a name="deallocate"></a> sync_per_thread::d еаллокате

Освобождает указанное число объектов из памяти, начиная с заданной позиции.

```cpp
void deallocate(void* ptr, std::size_t count);
```

### <a name="parameters"></a>Параметры

*указатель*\
Указатель на первый объект, который должен быть освобожден из хранилища.

*расчета*\
Количество объектов для освобождения из хранилища.

### <a name="remarks"></a>Комментарии

Функция-член вызывает метод `deallocate` в объекте кэша, который относится к текущему потоку. Если объект кэша для текущего потока не выделен, сначала такой объект будет выделен.

## <a name="sync_per_threadequals"></a><a name="equals"></a> sync_per_thread:: Equals

Сравнивает два кэша на равенство.

```cpp
bool equals(const sync<Cache>& Other) const;
```

### <a name="parameters"></a>Параметры

*Мбайта*\
Объект кэша фильтра синхронизации.

*Иной*\
Объект кэша для сравнения на равенство.

### <a name="return-value"></a>Возвращаемое значение

**`false`** значение, если объект кэша не был выделен для данного объекта или для *другого* в текущем потоке. В противном случае возвращается результат применения `operator==` к двум объектам кэша.

### <a name="remarks"></a>Комментарии

## <a name="see-also"></a>См. также раздел

[\<allocators>](../standard-library/allocators-header.md)
