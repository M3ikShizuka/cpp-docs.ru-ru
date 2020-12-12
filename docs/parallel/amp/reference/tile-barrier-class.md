---
description: 'Дополнительные сведения о: tile_barrier классе'
title: Класс tile_barrier
ms.date: 03/27/2019
f1_keywords:
- tile_barrier
- AMP/tile_barrier
- AMP/Concurrency::tile_barrier::tile_barrier::tile_barrier
- AMP/Concurrency::tile_barrier::tile_barrier::wait
- AMP/Concurrency::tile_barrier::tile_barrier::wait_with_all_memory_fence
- AMP/Concurrency::tile_barrier::tile_barrier::wait_with_global_memory_fence
- AMP/Concurrency::tile_barrier::tile_barrier::wait_with_tile_static_memory_fence
helpviewer_keywords:
- tile_barrier class
ms.assetid: b4ccdccb-0032-4e11-b7bd-dc9d43445dee
ms.openlocfilehash: b4fd1758f9786f4cbb78556daadb0801795ca9c3
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97321712"
---
# <a name="tile_barrier-class"></a>Класс tile_barrier

Синхронизирует выполнение потоков, выполняющихся в группе потоков (плитке), с помощью `wait` методов. Только среда выполнения может создать экземпляр этого класса.

## <a name="syntax"></a>Синтаксис

```cpp
class tile_barrier;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Конструктор tile_barrier](#ctor)|Инициализирует новый экземпляр класса `tile_barrier`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[ожидания](#wait)|Указывает всем потокам в группе потоков (плитке), что выполнение прекращается до завершения ожидания всех потоков в плитке.|
|[wait_with_all_memory_fence](#wait_with_all_memory_fence)|Блокирует выполнение всех потоков в плитке до тех пор, пока не будут завершены все доступ к памяти и все потоки в плитке достигли этого вызова.|
|[wait_with_global_memory_fence](#wait_with_global_memory_fence)|Блокирует выполнение всех потоков в плитке до тех пор, пока не завершится полный доступ к глобальной памяти и все потоки в плитке достигли этого вызова.|
|[wait_with_tile_static_memory_fence](#wait_with_tile_static_memory_fence)|Блокирует выполнение всех потоков в плитке до тех пор, пока не будут `tile_static` завершены все доступ к памяти и все потоки в плитке достигли этого вызова.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`tile_barrier`

## <a name="requirements"></a>Требования

**Заголовок** : amp.h

**Пространство имен** : Concurrency

## <a name="tile_barrier-constructor"></a><a name="ctor"></a> Конструктор tile_barrier

Инициализирует новый экземпляр класса путем копирования существующего.

### <a name="syntax"></a>Синтаксис

```cpp
tile_barrier(
    const tile_barrier& _Other ) restrict(amp,cpu);
```

### <a name="parameters"></a>Параметры

*_Other*<br/>
Копируемый объект `tile_barrier`.

## <a name="wait"></a>wait

Указывает всем потокам в группе потоков (плитке), что выполнение будет прервано до завершения ожидания всех потоков в плитке.

### <a name="syntax"></a>Синтаксис

```cpp
void wait() const restrict(amp);
```

## <a name="wait_with_all_memory_fence"></a><a name="wait_with_all_memory_fence"></a> wait_with_all_memory_fence

Блокирует выполнение всех потоков в плитке до тех пор, пока все потоки в плитке не достигли этого вызова. Это гарантирует, что все доступ к памяти будут видны другим потокам в плитке потока и выполнены в порядке программ.

### <a name="syntax"></a>Синтаксис

```cpp
void wait_with_all_memory_fence() const restrict(amp);
```

## <a name="a-namewait_with_global_memory_fence-wait_with_global_memory_fence"></a><a name="wait_with_global_memory_fence"> wait_with_global_memory_fence

Блокирует выполнение всех потоков в плитке до тех пор, пока все потоки в плитке не достигли этого вызова. Это гарантирует, что все доступ к глобальной памяти будут видны другим потокам в плитке потока и выполнены в порядке программ.

### <a name="syntax"></a>Синтаксис

```cpp
void wait_with_global_memory_fence() const  restrict(amp);
```

## <a name="a-namewait_with_tile_static_memory_fence-wait_with_tile_static_memory_fence"></a><a name="wait_with_tile_static_memory_fence"> wait_with_tile_static_memory_fence

Блокирует выполнение всех потоков в плитке до тех пор, пока все потоки в плитке не достигли этого вызова. Это гарантирует, что `tile_static` доступ к памяти будет виден другим потокам в плитке потока и выполнен в порядке программ.

### <a name="syntax"></a>Синтаксис

```cpp
void wait_with_tile_static_memory_fence() const restrict(amp);
```

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency (C++ AMP)](concurrency-namespace-cpp-amp.md)
