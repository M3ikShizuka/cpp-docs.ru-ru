---
description: 'Дополнительные сведения о: max_variable_size классе'
title: Класс max_variable_size
ms.date: 11/04/2016
f1_keywords:
- allocators/stdext::max_variable_size
- allocators/stdext::max_variable_size::allocated
- allocators/stdext::max_variable_size::deallocated
- allocators/stdext::max_variable_size::full
- allocators/stdext::max_variable_size::released
- allocators/stdext::max_variable_size::saved
helpviewer_keywords:
- stdext::max_variable_size
- stdext::max_variable_size [C++], allocated
- stdext::max_variable_size [C++], deallocated
- stdext::max_variable_size [C++], full
- stdext::max_variable_size [C++], released
- stdext::max_variable_size [C++], saved
ms.assetid: 9f2e9df0-4148-4b37-bc30-f8eca0ef86ae
ms.openlocfilehash: 0640e11e4ab68b60dc8114c88463a370e43dc749
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97149231"
---
# <a name="max_variable_size-class"></a>Класс max_variable_size

Описывает объект [max class](../standard-library/allocators-header.md), который ограничивает максимальную длину объекта [freelist](../standard-library/freelist-class.md) до значения, приблизительно пропорционального количеству выделенных блоков памяти.

## <a name="syntax"></a>Синтаксис

```cpp
class max_variable_size
```

### <a name="constructors"></a>Конструкторы

|Конструктор|Описание|
|-|-|
|[max_variable_size](#max_variable_size)|Создает объект типа `max_variable_size`.|

### <a name="member-functions"></a>Функции элементов

|Функция-член|Описание|
|-|-|
|[allocated](#allocated)|Увеличивает счетчик выделенных блоков памяти.|
|[освобождена](#deallocated)|Уменьшает счетчик выделенных блоков памяти.|
|[full](#full)|Возвращает значение, указывающее, следует ли добавить дополнительные блоки памяти для свободного списка.|
|[освободил](#released)|Уменьшает количество блоков памяти в свободном списке.|
|[saved](#saved)|Увеличивает количество блоков памяти в свободном списке.|

## <a name="requirements"></a>Требования

**Заголовок:**\<allocators>

**Пространство имен:** stdext

## <a name="max_variable_sizeallocated"></a><a name="allocated"></a> max_variable_size:: выделено

Увеличивает счетчик выделенных блоков памяти.

```cpp
void allocated(std::size_t _Nx = 1);
```

### <a name="parameters"></a>Параметры

*_Nx*\
Значение приращения.

### <a name="remarks"></a>Комментарии

Эта функция члена добавляет *_Nx* к сохраненному значению `_Nallocs` . Эта функция-член вызывается после каждого успешного вызова `cache_freelist::allocate` оператором **`new`** . Аргумент *_Nx* — число блоков памяти в блоке, выделенном оператором **`new`** .

## <a name="max_variable_sizedeallocated"></a><a name="deallocated"></a> max_variable_size::d еаллокатед

Уменьшает счетчик выделенных блоков памяти.

```cpp
void deallocated(std::size_t _Nx = 1);
```

### <a name="parameters"></a>Параметры

*_Nx*\
Значение приращения.

### <a name="remarks"></a>Комментарии

Функция члена вычитает *_Nx* из сохраненного значения `_Nallocs` . Эта функция-член вызывается после каждого вызова `cache_freelist::deallocate` оператором **`delete`** . Аргумент *_Nx* — число блоков памяти в блоке, освобожденных оператором **`delete`** .

## <a name="max_variable_sizefull"></a><a name="full"></a> max_variable_size:: Full

Возвращает значение, указывающее, следует ли добавить дополнительные блоки памяти для свободного списка.

```cpp
bool full();
```

### <a name="return-value"></a>Возвращаемое значение

**`true`** Если `_Nallocs / 16 + 16 <= _Nblocks` .

### <a name="remarks"></a>Комментарии

Эта функция-член вызывается `cache_freelist::deallocate`. Если вызов возвращает **`true`** , `deallocate` помещает блок памяти в свободный список; если возвращается значение false, `deallocate` вызывает оператор **`delete`** для освобождения блока.

## <a name="max_variable_sizemax_variable_size"></a><a name="max_variable_size"></a> max_variable_size:: max_variable_size

Создает объект типа `max_variable_size`.

```cpp
max_variable_size();
```

### <a name="remarks"></a>Комментарии

Конструктор инициализирует сохраненные значения `_Nblocks` и `_Nallocs` нулями.

## <a name="max_variable_sizereleased"></a><a name="released"></a> max_variable_size:: Released

Уменьшает количество блоков памяти в свободном списке.

```cpp
void released();
```

### <a name="remarks"></a>Комментарии

Эта функция-член уменьшает хранимое значение `_Nblocks`. Функция-член `released` текущего класса max вызывается `cache_freelist::allocate` каждый раз при удалении блока памяти из свободного списка.

## <a name="max_variable_sizesaved"></a><a name="saved"></a> max_variable_size:: сохранен

Увеличивает количество блоков памяти в свободном списке.

```cpp
void saved();
```

### <a name="remarks"></a>Комментарии

Эта функция-член увеличивает хранимое значение `_Nblocks`. Она вызывается `cache_freelist::deallocate` каждый раз при помещении блока памяти в свободный список.

## <a name="see-also"></a>См. также раздел

[\<allocators>](../standard-library/allocators-header.md)
