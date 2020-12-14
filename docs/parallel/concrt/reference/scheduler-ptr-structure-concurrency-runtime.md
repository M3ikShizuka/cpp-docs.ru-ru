---
description: 'Дополнительные сведения: структура scheduler_ptr'
title: Структура scheduler_ptr
ms.date: 11/04/2016
f1_keywords:
- scheduler_ptr
- PPLINTERFACE/concurrency::scheduler_ptr
- PPLINTERFACE/concurrency::scheduler_ptr::scheduler_ptr::scheduler_ptr
- PPLINTERFACE/concurrency::scheduler_ptr::scheduler_ptr::get
- PPLINTERFACE/concurrency::scheduler_ptr::scheduler_ptr::operator bool
ms.assetid: e88c84af-c306-476d-aef1-f42a0fa0a80f
ms.openlocfilehash: 314f587c0fd55772a8b1b7b5b8fdf3ddeb53a7a9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97188785"
---
# <a name="scheduler_ptr-structure"></a>Структура scheduler_ptr

Представляет указатель на планировщик. Этот класс существует, чтобы разрешить спецификацию общего времени существования с помощью shared_ptr или просто простой ссылки с помощью необработанного указателя.

## <a name="syntax"></a>Синтаксис

```cpp
struct scheduler_ptr;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[scheduler_ptr:: scheduler_ptr](#ctor)|Перегружен. Создает указатель планировщика из shared_ptr планировщику|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[scheduler_ptr:: Get](#get)|Возвращает необработанный указатель планировщику|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[scheduler_ptr:: operator bool](#operator_bool)|Проверьте, является ли указатель планировщика отличным от null|
|[scheduler_ptr:: operator —&gt;](#operator_ptr)|Поведение, как у указателя|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`scheduler_ptr`

## <a name="requirements"></a>Требования

**Заголовок:** пплинтерфаце. h

**Пространство имен:** параллелизм

## <a name="scheduler_ptrget-method"></a><a name="get"></a> Метод scheduler_ptr:: Get

Возвращает необработанный указатель на планировщик.

```cpp
scheduler_interface* get() const;
```

### <a name="return-value"></a>Возвращаемое значение

## <a name="scheduler_ptroperator-bool"></a><a name="operator_bool"></a> scheduler_ptr:: operator bool

Проверяет, имеет ли указатель планировщика значение, отличное от NULL.

```cpp
operator bool() const;
```

## <a name="scheduler_ptroperator-gt"></a><a name="operator_ptr"></a> scheduler_ptr:: operator —&gt;

Ведет себя как указатель.

```cpp
scheduler_interface* operator->() const;
```

### <a name="return-value"></a>Возвращаемое значение

## <a name="scheduler_ptrscheduler_ptr-constructor"></a><a name="ctor"></a> Конструктор scheduler_ptr:: scheduler_ptr

Создает указатель планировщика из shared_ptr в планировщик.

```cpp
explicit scheduler_ptr(std::shared_ptr<scheduler_interface> scheduler);
explicit scheduler_ptr(_In_opt_ scheduler_interface* pScheduler);
```

### <a name="parameters"></a>Параметры

*планировщика*<br/>
Планировщик для преобразования.

*псчедулер*<br/>
Указатель планировщика для преобразования.

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency](concurrency-namespace.md)
