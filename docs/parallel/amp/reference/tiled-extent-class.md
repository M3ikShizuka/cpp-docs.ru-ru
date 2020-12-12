---
description: 'Дополнительные сведения о: tiled_extent классе'
title: Класс tiled_extent
ms.date: 11/04/2016
f1_keywords:
- tiled_extent
- AMP/tiled_extent
- AMP/Concurrency::tiled_extent::tiled_extent
- AMP/Concurrency::tiled_extent::get_tile_extent
- AMP/Concurrency::tiled_extent::pad
- AMP/Concurrency::tiled_extent::truncate
- AMP/Concurrency::tiled_extent::tile_dim0
- AMP/Concurrency::tiled_extent::tile_dim1
- AMP/Concurrency::tiled_extent::tile_dim2
- AMP/Concurrency::tiled_extent::tile_extent
ms.assetid: 671ecaf8-c7b0-4ac8-bbdc-e30bd92da7c0
ms.openlocfilehash: ca5b5c630152263ca49adf5c201ee0b892a192c2
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97163877"
---
# <a name="tiled_extent-class"></a>Класс tiled_extent

`tiled_extent`Объект — это `extent` объект от одного до трех измерений, который делит пространство экстента на одно, две или трехмерные плитки.

## <a name="syntax"></a>Синтаксис

```cpp
template <
    int _Dim0,
    int _Dim1,
    int _Dim2
>
class tiled_extent : public Concurrency::extent<3>;

template <
    int _Dim0,
    int _Dim1
>
class tiled_extent<_Dim0, _Dim1, 0> : public Concurrency::extent<2>;

template <
    int _Dim0
>
class tiled_extent<_Dim0, 0, 0> : public Concurrency::extent<1>;
```

### <a name="parameters"></a>Параметры

*_Dim0*<br/>
Длина наиболее значимого измерения.

*_Dim1*<br/>
Длина последующего и значительного измерения.

*_Dim2*<br/>
Длина наименее значимого измерения.

## <a name="members"></a>Элементы

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Конструктор tiled_extent](#ctor)|Инициализирует новый экземпляр класса `tiled_extent`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[get_tile_extent](#get_tile_extent)|Возвращает `extent` объект, который фиксирует значения `tiled_extent` аргументов шаблона `_Dim0` , `_Dim1` и `_Dim2` .|
|[коммутаци](#pad)|Возвращает новый `tiled_extent` объект с экстентами, настройкой которых равномерно делится на размеры мозаики.|
|[truncate](#truncate)|Возвращает новый `tiled_extent` объект с разворачивающимися экстентами, которые равномерно делятся по измерениям мозаики.|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[Оператор =](#operator_eq)|Копирует содержимое указанного `tiled_index` объекта в этот объект.|

### <a name="public-constants"></a>Открытые константы

|Имя|Описание|
|----------|-----------------|
|[Константа tile_dim0](#tile_dim0)|Хранит длину наиболее значимого измерения.|
|[Константа tile_dim1](#tile_dim1)|Сохраняет длину последующего и значительного измерения.|
|[Константа tile_dim2](#tile_dim2)|Хранит длину наименее значимого измерения.|

### <a name="public-data-members"></a>Открытые члены данных

|Имя|Описание|
|----------|-----------------|
|[tile_extent](#tile_extent)|Возвращает `extent` объект, который фиксирует значения `tiled_extent` аргументов шаблона `_Dim0` , `_Dim1` и `_Dim2` .|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`extent`

`tiled_extent`

## <a name="requirements"></a>Требования

**Заголовок** : amp.h

**Пространство имен** : Concurrency

## <a name="tiled_extent-constructor"></a><a name="ctor"></a> конструктор tiled_extent

Инициализирует новый экземпляр класса `tiled_extent`.

### <a name="syntax"></a>Синтаксис

```cpp
tiled_extent();

tiled_extent(
    const Concurrency::extent<rank>& _Other );

tiled_extent(
    const tiled_extent& _Other );
```

### <a name="parameters"></a>Параметры

*_Other*<br/>
`extent` `tiled_extent` Копируемый объект или.

## <a name="get_tile_extent"></a><a name="get_tile_extent"></a> get_tile_extent

Возвращает `extent` объект, который фиксирует значения `tiled_extent` аргументов шаблона `_Dim0` , `_Dim1` и `_Dim2` .

### <a name="syntax"></a>Синтаксис

```cpp
Concurrency::extent<rank> get_tile_extent() const restrict(amp,cpu);
```

### <a name="return-value"></a>Возвращаемое значение

`extent`Объект, который фиксирует размеры данного `tiled_extent` экземпляра.

## <a name="pad"></a><a name="pad"></a> панель

Возвращает новый `tiled_extent` объект с экстентами, настройкой которых равномерно делится на размеры мозаики.

### <a name="syntax"></a>Синтаксис

```cpp
tiled_extent pad() const;
```

### <a name="return-value"></a>Возвращаемое значение

Новый `tiled_extent` объект по значению.

## <a name="truncate"></a><a name="truncate"></a> усечение

Возвращает новый `tiled_extent` объект с разворачивающимися экстентами, которые равномерно делятся по измерениям мозаики.

### <a name="syntax"></a>Синтаксис

```cpp
tiled_extent truncate() const;
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает новый `tiled_extent` объект с разворачивающимися экстентами, которые равномерно делятся по измерениям мозаики.

## <a name="operator"></a><a name="operator_eq"></a> оператор =

Копирует содержимое указанного `tiled_index` объекта в этот объект.

### <a name="syntax"></a>Синтаксис

```cpp
tiled_extent&  operator= (
    const tiled_extent& _Other ) restrict (amp, cpu);
```

### <a name="parameters"></a>Параметры

*_Other*<br/>
Объект, из которого производится `tiled_index` копирование.

### <a name="return-value"></a>Возвращаемое значение

Ссылка на этот `tiled_index` экземпляр.

## <a name="tile_dim0"></a><a name="tile_dim0"></a> tile_dim0

Хранит длину наиболее значимого измерения.

### <a name="syntax"></a>Синтаксис

```cpp
static const int tile_dim0 = _Dim0;
```

## <a name="tile_dim1"></a><a name="tile_dim1"></a> tile_dim1

Сохраняет длину последующего и значительного измерения.

### <a name="syntax"></a>Синтаксис

```cpp
static const int tile_dim1 = _Dim1;
```

## <a name="tile_dim2"></a><a name="tile_dim2"></a> tile_dim2

Хранит длину наименее значимого измерения.

### <a name="syntax"></a>Синтаксис

```cpp
static const int tile_dim2 = _Dim2;
```

## <a name="tile_extent"></a><a name="tile_extent"></a> tile_extent

Возвращает `extent` объект, который фиксирует значения `tiled_extent` аргументов шаблона `_Dim0` , `_Dim1` и `_Dim2` .

### <a name="syntax"></a>Синтаксис

```cpp
__declspec(property(get= get_tile_extent)) Concurrency::extent<rank> tile_extent;
```

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency (C++ AMP)](concurrency-namespace-cpp-amp.md)
