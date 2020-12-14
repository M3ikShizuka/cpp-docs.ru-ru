---
description: Дополнительные сведения о классе Message
title: Класс message
ms.date: 11/04/2016
f1_keywords:
- message
- AGENTS/concurrency::message
- AGENTS/concurrency::message::message
- AGENTS/concurrency::message::add_ref
- AGENTS/concurrency::message::msg_id
- AGENTS/concurrency::message::remove_ref
- AGENTS/concurrency::message::payload
helpviewer_keywords:
- message class
ms.assetid: 3e1f3505-6c0c-486c-8191-666d0880ec62
ms.openlocfilehash: 0e15dafd9606e68f7a6ed1bed3795791c0f6870c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97202318"
---
# <a name="message-class"></a>Класс message

Основной конверт сообщения, содержащий полезные данные, передаваемые между блоками обмена сообщениями.

## <a name="syntax"></a>Синтаксис

```cpp
template<class T>
class message : public ::Concurrency::details::_Runtime_object;
```

### <a name="parameters"></a>Параметры

*T*<br/>
Тип данных полезной нагрузки в сообщении.

## <a name="members"></a>Элементы

### <a name="public-typedefs"></a>Общедоступные определения типов

|Имя|Описание|
|----------|-----------------|
|`type`|Псевдоним типа для `T` .|

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[message](#ctor)|Перегружен. Формирует объект `message`.|
|[Деструктор сообщений ~](#dtor)|Уничтожает `message` объект.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[add_ref](#add_ref)|Добавляет к счетчику ссылок для `message` объекта. Используется для блоков сообщений, требующих подсчета ссылок для определения времени существования сообщений.|
|[msg_id](#msg_id)|Возвращает идентификатор `message` объекта.|
|[remove_ref](#remove_ref)|Вычитает из счетчика ссылок для `message` объекта. Используется для блоков сообщений, требующих подсчета ссылок для определения времени существования сообщений.|

### <a name="public-data-members"></a>Открытые члены данных

|Имя|Описание|
|----------|-----------------|
|[полезных данных](#payload)|Полезные данные `message` объекта.|

## <a name="remarks"></a>Комментарии

Дополнительные сведения см. в разделе [асинхронные блоки сообщений](../../../parallel/concrt/asynchronous-message-blocks.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`message`

## <a name="requirements"></a>Требования

**Заголовок:** agents.h

**Пространство имен:** параллелизм

## <a name="add_ref"></a><a name="add_ref"></a> add_ref

Добавляет к счетчику ссылок для `message` объекта. Используется для блоков сообщений, требующих подсчета ссылок для определения времени существования сообщений.

```cpp
long add_ref();
```

### <a name="return-value"></a>Возвращаемое значение

Новое значение счетчика ссылок.

## <a name="message"></a><a name="ctor"></a> Сообщение

Формирует объект `message`.

```cpp
message(
    T const& _P);

message(
    T const& _P,
    runtime_object_identity _Id);

message(
    message const& _Msg);

message(
    _In_ message const* _Msg);
```

### <a name="parameters"></a>Параметры

*_P*<br/>
Полезная нагрузка этого сообщения.

*_Id*<br/>
Уникальный идентификатор этого сообщения.

*_Msg*<br/>
Ссылка или указатель на `message` объект.

### <a name="remarks"></a>Комментарии

Конструктор, принимающий указатель на `message` объект в качестве аргумента, вызывает исключение [invalid_argument](../../../standard-library/invalid-argument-class.md) , если параметр `_Msg` имеет значение `NULL` .

## <a name="message"></a><a name="dtor"></a> сообщение ~

Уничтожает `message` объект.

```cpp
virtual ~message();
```

## <a name="msg_id"></a><a name="msg_id"></a> msg_id

Возвращает идентификатор `message` объекта.

```cpp
runtime_object_identity msg_id() const;
```

### <a name="return-value"></a>Возвращаемое значение

Свойство `runtime_object_identity` объекта `message`.

## <a name="payload"></a><a name="payload"></a> полезных данных

Полезные данные `message` объекта.

```cpp
T const payload;
```

## <a name="remove_ref"></a><a name="remove_ref"></a> remove_ref

Вычитает из счетчика ссылок для `message` объекта. Используется для блоков сообщений, требующих подсчета ссылок для определения времени существования сообщений.

```cpp
long remove_ref();
```

### <a name="return-value"></a>Возвращаемое значение

Новое значение счетчика ссылок.

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency](concurrency-namespace.md)
