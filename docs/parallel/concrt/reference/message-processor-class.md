---
description: 'Дополнительные сведения о: message_processor классе'
title: Класс message_processor
ms.date: 11/04/2016
f1_keywords:
- message_processor
- AGENTS/concurrency::message_processor
- AGENTS/concurrency::message_processor::async_send
- AGENTS/concurrency::message_processor::sync_send
- AGENTS/concurrency::message_processor::wait
- AGENTS/concurrency::message_processor::process_incoming_message
helpviewer_keywords:
- message_processor class
ms.assetid: 23afb052-daa7-44ed-bf24-d2513db748da
ms.openlocfilehash: f74314bde6e12ea8b00bfc7bfd2567ca15864f75
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97202201"
---
# <a name="message_processor-class"></a>Класс message_processor

Класс `message_processor` — это абстрактный базовый класс для обработки объектов `message`. Упорядочивание сообщений не гарантируется.

## <a name="syntax"></a>Синтаксис

```cpp
template<class T>
class message_processor;
```

### <a name="parameters"></a>Параметры

*T*<br/>
Тип данных полезной нагрузки в сообщениях, обрабатываемых этим `message_processor` объектом.

## <a name="members"></a>Элементы

### <a name="public-typedefs"></a>Общедоступные определения типов

|Имя|Описание|
|----------|-----------------|
|`type`|Псевдоним типа для `T` .|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[async_send](#async_send)|При переопределении в производном классе помещает сообщения в блок асинхронно.|
|[sync_send](#sync_send)|При переопределении в производном классе помещает сообщения в блок синхронно.|
|[ожидания](#wait)|При переопределении в производном классе ожидает завершения всех асинхронных операций.|

### <a name="protected-methods"></a>Защищенные методы

|Имя|Описание|
|----------|-----------------|
|[process_incoming_message](#process_incoming_message)|При переопределении в производном классе выполняет прямую обработку сообщений в блок. Вызывается каждый раз при добавлении нового сообщения, если очередь пуста.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`message_processor`

## <a name="requirements"></a>Требования

**Заголовок:** agents.h

**Пространство имен:** параллелизм

## <a name="async_send"></a><a name="async_send"></a> async_send

При переопределении в производном классе помещает сообщения в блок асинхронно.

```cpp
virtual void async_send(_Inout_opt_ message<T>* _Msg) = 0;
```

### <a name="parameters"></a>Параметры

*_Msg*<br/>
`message`Объект для асинхронной отправки.

### <a name="remarks"></a>Комментарии

Реализация процессора должна переопределять этот метод.

## <a name="process_incoming_message"></a><a name="process_incoming_message"></a> process_incoming_message

При переопределении в производном классе выполняет прямую обработку сообщений в блок. Вызывается каждый раз при добавлении нового сообщения, если очередь пуста.

```cpp
virtual void process_incoming_message() = 0;
```

### <a name="remarks"></a>Комментарии

Реализации блоков сообщений должны переопределять этот метод.

## <a name="sync_send"></a><a name="sync_send"></a> sync_send

При переопределении в производном классе помещает сообщения в блок синхронно.

```cpp
virtual void sync_send(_Inout_opt_ message<T>* _Msg) = 0;
```

### <a name="parameters"></a>Параметры

*_Msg*<br/>
`message`Объект для синхронной отправки.

### <a name="remarks"></a>Комментарии

Реализация процессора должна переопределять этот метод.

## <a name="wait"></a><a name="wait"></a> ожидания

При переопределении в производном классе ожидает завершения всех асинхронных операций.

```cpp
virtual void wait() = 0;
```

### <a name="remarks"></a>Комментарии

Реализация процессора должна переопределять этот метод.

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency](concurrency-namespace.md)<br/>
[Класс ordered_message_processor](ordered-message-processor-class.md)
