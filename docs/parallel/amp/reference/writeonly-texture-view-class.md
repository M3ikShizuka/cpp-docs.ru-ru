---
description: 'Дополнительные сведения о: writeonly_texture_view классе'
title: Класс writeonly_texture_view
ms.date: 11/04/2016
f1_keywords:
- writeonly_texture_view
- AMP_GRAPHICS/writeonly_texture_view
- AMP_GRAPHICS/Concurrency::graphics::writeonly_texture_view
- AMP_GRAPHICS/Concurrency::graphics::writeonly_texture_view::set
- AMP_GRAPHICS/Concurrency::graphics::rank Constant
ms.assetid: 8d117ad3-0a1c-41ae-b29c-7c95fdd4d04d
ms.openlocfilehash: 17e9ed49c5fb3c976343d8c3ad8690d7f41b166d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97314526"
---
# <a name="writeonly_texture_view-class"></a>Класс writeonly_texture_view

Предоставляет WriteOnly доступ к текстуре.

## <a name="syntax"></a>Синтаксис

```cpp
template <
    typename value_type,
    int _Rank
>
class writeonly_texture_view;

template <
    typename value_type,
    int _Rank
>
class writeonly_texture_view<value_type, _Rank> : public details::_Texture_base<value_type, _Rank>;
```

### <a name="parameters"></a>Параметры

*value_type*<br/>
Тип элементов текстуры.

*_Rank*<br/>
Ранг текстуры.

## <a name="members"></a>Элементы

### <a name="public-typedefs"></a>Общедоступные определения типов

|Имя|Описание|
|----------|-----------------|
|`scalar_type`||
|`value_type`|Тип элементов текстуры.|

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Конструктор writeonly_texture_view](#ctor)|Инициализирует новый экземпляр класса `writeonly_texture_view`.|
|[Деструктор ~ writeonly_texture_view](#ctor)|Уничтожает `writeonly_texture_view` объект.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[set](#set)|Задает значение элемента по указанному индексу.|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[Оператор =](#operator_eq)|Копирует указанный `writeonly_texture_view` объект в этот элемент.|

### <a name="public-constants"></a>Открытые константы

|Имя|Описание|
|----------|-----------------|
|[Константа Rank](#rank)|Возвращает ранг `writeonly_texture_view` объекта.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`_Texture_base`

`writeonly_texture_view`

## <a name="requirements"></a>Требования

**Заголовок:** amp_graphics. h

**Пространство имен:** Concurrency:: Graphics

## <a name="writeonly_texture_view"></a><a name="dtor"></a> ~ writeonly_texture_view

Уничтожает `writeonly_texture_view` объект.

```cpp
~writeonly_texture_view() restrict(amp,cpu);
```

## <a name="operator"></a><a name="operator_eq"></a> Оператор =

Копирует указанный `writeonly_texture_view` объект в этот элемент.

```cpp
writeonly_texture_view<value_type, _Rank>& operator= (
    const writeonly_texture_view<value_type, _Rank>& _Other) restrict(amp,cpu);
```

### <a name="parameters"></a>Параметры

*_Other*<br/>
`writeonly_texture_view` Объект, из которого производится копирование.

### <a name="return-value"></a>Возвращаемое значение

Ссылка на этот `writeonly_texture_view` объект.

## <a name="rank"></a><a name="rank"></a> Рейтинг

Возвращает ранг `writeonly_texture_view` объекта.

```cpp
static const int rank = _Rank;
```

## <a name="set"></a><a name="set"></a> параметр

Задает значение элемента по указанному индексу.

```cpp
void set(
    const index<_Rank>& _Index,
    const value_type& value) const restrict(amp);
```

### <a name="parameters"></a>Параметры

*_Index*<br/>
Индекс элемента.

*value*<br/>
Новое значение элемента.

## <a name="writeonly_texture_view"></a><a name="ctor"></a> writeonly_texture_view

Инициализирует новый экземпляр класса `writeonly_texture_view`.

```cpp
writeonly_texture_view(
    texture<value_type,
    _Rank>& _Src) restrict(amp);

writeonly_texture_view(
    const writeonly_texture_view<value_type,
    _Rank>& _Src) restrict(amp,cpu);
```

### <a name="parameters"></a>Параметры

*_Rank*<br/>
Ранг текстуры.

*value_type*<br/>
Тип элементов текстуры.

*_Src*<br/>
Текстура, используемая для создания `writeonly_texture_view` .

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency::graphics](concurrency-graphics-namespace.md)
