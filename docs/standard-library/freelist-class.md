---
description: 'Дополнительные сведения о: freelist Class'
title: Класс freelist
ms.date: 11/04/2016
f1_keywords:
- allocators/stdext::freelist
- allocators/stdext::freelist::pop
- allocators/stdext::freelist::push
helpviewer_keywords:
- stdext::freelist
- stdext::freelist [C++], pop
- stdext::freelist [C++], push
ms.assetid: 8ad7e35c-4c80-4479-8ede-1a2497b06d71
ms.openlocfilehash: de0803aac13138dc25116084f52e7a5bea694b41
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97324373"
---
# <a name="freelist-class"></a>Класс freelist

Управляет списком блоков памяти.

## <a name="syntax"></a>Синтаксис

```cpp
template <std::size_t Sz, class Max>
class freelist : public Max
```

### <a name="parameters"></a>Параметры

*SZ*\
Число выделяемых элементов в массиве.

*Максимальной*\
Класс max, представляющий максимальное количество элементов, которые необходимо сохранить в свободном списке. Классом max может быть [max_none](../standard-library/max-none-class.md), [max_unbounded](../standard-library/max-unbounded-class.md), [max_fixed_size](../standard-library/max-fixed-size-class.md) или [max_variable_size](../standard-library/max-variable-size-class.md).

## <a name="remarks"></a>Комментарии

Этот шаблон класса управляет списком блоков памяти размером *SZ* с максимальной длиной списка, определяемой классом Max, который передается *Max*.

### <a name="constructors"></a>Конструкторы

|Конструктор|Описание|
|-|-|
|[freelist](#freelist)|Создает объект типа `freelist`.|

### <a name="member-functions"></a>Функции элементов

|Функция-член|Описание|
|-|-|
|[pop](#pop)|Удаляет первый блок памяти из свободного списка.|
|[push](#push)|Добавляет блок памяти в список.|

## <a name="requirements"></a>Требования

**Заголовок:**\<allocators>

**Пространство имен:** stdext

## <a name="freelistfreelist"></a><a name="freelist"></a> freelist:: freelist

Создает объект типа `freelist`.

```cpp
freelist();
```

### <a name="remarks"></a>Комментарии

## <a name="freelistpop"></a><a name="pop"></a> freelist::p Op

Удаляет первый блок памяти из свободного списка.

```cpp
void *pop();
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает указатель на блок памяти, удаленный из списка.

### <a name="remarks"></a>Комментарии

Функция-член возвращает значение NULL, если список пуст. В противном случае удаляет первый блок памяти из списка.

## <a name="freelistpush"></a><a name="push"></a> freelist::p тельную

Добавляет блок памяти в список.

```cpp
bool push(void* ptr);
```

### <a name="parameters"></a>Параметры

*указатель*\
Указатель на блок памяти, которые необходимо добавить в свободный список.

### <a name="return-value"></a>Возвращаемое значение

**`true`**`full`значение, если функция класса max Возвращает **`false`** . в противном случае `push` функция возвращает значение **`false`** .

### <a name="remarks"></a>Комментарии

Если `full` функция класса max Возвращает **`false`** , эта функция-член добавляет блок памяти, на который указывает *ptr* , в заголовок списка.

## <a name="see-also"></a>См. также раздел

[\<allocators>](../standard-library/allocators-header.md)
