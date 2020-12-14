---
description: 'Дополнительные сведения о: target_block классе'
title: Класс target_block
ms.date: 11/04/2016
f1_keywords:
- target_block
- AGENTS/concurrency::target_block
- AGENTS/concurrency::target_block::target_block
- AGENTS/concurrency::target_block::propagate
- AGENTS/concurrency::target_block::send
- AGENTS/concurrency::target_block::async_send
- AGENTS/concurrency::target_block::decline_incoming_messages
- AGENTS/concurrency::target_block::enable_batched_processing
- AGENTS/concurrency::target_block::initialize_target
- AGENTS/concurrency::target_block::link_source
- AGENTS/concurrency::target_block::process_input_messages
- AGENTS/concurrency::target_block::process_message
- AGENTS/concurrency::target_block::propagate_message
- AGENTS/concurrency::target_block::register_filter
- AGENTS/concurrency::target_block::remove_sources
- AGENTS/concurrency::target_block::send_message
- AGENTS/concurrency::target_block::sync_send
- AGENTS/concurrency::target_block::unlink_source
- AGENTS/concurrency::target_block::unlink_sources
- AGENTS/concurrency::target_block::wait_for_async_sends
helpviewer_keywords:
- target_block class
ms.assetid: 3ce181b4-b94a-4894-bf7b-64fc09821f9f
ms.openlocfilehash: 0860ff7b185eef997d7c76f61d67ad10056ca9cc
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97188421"
---
# <a name="target_block-class"></a>Класс target_block

Класс `target_block` — это абстрактный базовый класс, который предоставляет основные функции управления соединениями и проверку ошибок только для целевых блоков.

## <a name="syntax"></a>Синтаксис

```cpp
template<class _SourceLinkRegistry, class _MessageProcessorType = ordered_message_processor<typename _SourceLinkRegistry::type::source_type>>
class target_block : public ITarget<typename _SourceLinkRegistry::type::source_type>;
```

### <a name="parameters"></a>Параметры

*_SourceLinkRegistry*<br/>
Реестр ссылок, используемый для хранения исходных ссылок.

*_MessageProcessorType*<br/>
Тип процессора для обработки сообщений.

## <a name="members"></a>Элементы

### <a name="public-typedefs"></a>Общедоступные определения типов

|Имя|Описание|
|----------|-----------------|
|`source_iterator`|Тип итератора для `source_link_manager` для данного `target_block` объекта.|

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[target_block](#ctor)|Формирует объект `target_block`.|
|[Деструктор ~ target_block](#dtor)|Уничтожает `target_block` объект.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[распространения](#propagate)|Асинхронно передает сообщение из исходного блока в этот целевой блок.|
|[send](#send)|Синхронно передает сообщение из исходного блока в этот целевой блок.|

### <a name="protected-methods"></a>Защищенные методы

|Имя|Описание|
|----------|-----------------|
|[async_send](#async_send)|Асинхронно отправляет сообщение для обработки.|
|[decline_incoming_messages](#decline_incoming_messages)|Указывает блоку, что следует отклонять новые сообщения.|
|[enable_batched_processing](#enable_batched_processing)|Активирует пакетную обработку для этого блока.|
|[initialize_target](#initialize_target)|Инициализирует базовый объект. В частности, необходимо `message_processor` инициализировать объект.|
|[link_source](#link_source)|Связывает указанный блок источника с этим `target_block` объектом.|
|[process_input_messages](#process_input_messages)|Обрабатывает сообщения, полученные как входные данные.|
|[process_message](#process_message)|При переопределении в производном классе обрабатывает сообщение, которое ранее было принято данным объектом `target_block`.|
|[propagate_message](#propagate_message)|При переопределении в производном классе этот метод асинхронно передает сообщение из `ISource` блока в этот `target_block` объект. Он вызывается `propagate` методом при вызове из исходного блока.|
|[register_filter](#register_filter)|Регистрирует метод фильтра, который будет вызываться для каждого полученного сообщения.|
|[remove_sources](#remove_sources)|Отменяет связь со всеми источниками после ожидания завершения ожидающих асинхронных операций отправки.|
|[send_message](#send_message)|При переопределении в производном классе этот метод синхронно передает сообщение из `ISource` блока в этот `target_block` объект. Он вызывается `send` методом при вызове из исходного блока.|
|[sync_send](#sync_send)|Синхронная Отправка сообщения для обработки.|
|[unlink_source](#unlink_source)|Отменяет связь указанного исходного блока с этим `target_block` объектом.|
|[unlink_sources](#unlink_sources)|Отменяет связь со всеми исходными блоками этого `target_block` объекта. (Переопределяет метод [ITarget:: unlink_sources](itarget-class.md#unlink_sources).)|
|[wait_for_async_sends](#wait_for_async_sends)|Ожидает завершения всех асинхронных распространителей.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[ITarget](itarget-class.md)

`target_block`

## <a name="requirements"></a>Требования

**Заголовок:** agents.h

**Пространство имен:** параллелизм

## <a name="async_send"></a><a name="async_send"></a> async_send

Асинхронно отправляет сообщение для обработки.

```cpp
void async_send(_Inout_opt_ message<_Source_type>* _PMessage);
```

### <a name="parameters"></a>Параметры

*_PMessage*<br/>
Указатель на отправляемое сообщение.

## <a name="decline_incoming_messages"></a><a name="decline_incoming_messages"></a> decline_incoming_messages

Указывает блоку, что следует отклонять новые сообщения.

```cpp
void decline_incoming_messages();
```

### <a name="remarks"></a>Комментарии

Этот метод вызывается деструктором, чтобы гарантировать отклонение новых сообщений в процессе уничтожения.

## <a name="enable_batched_processing"></a><a name="enable_batched_processing"></a> enable_batched_processing

Активирует пакетную обработку для этого блока.

```cpp
void enable_batched_processing();
```

## <a name="initialize_target"></a><a name="initialize_target"></a> initialize_target

Инициализирует базовый объект. В частности, необходимо `message_processor` инициализировать объект.

```cpp
void initialize_target(
    _Inout_opt_ Scheduler* _PScheduler = NULL,
    _Inout_opt_ ScheduleGroup* _PScheduleGroup = NULL);
```

### <a name="parameters"></a>Параметры

*_PScheduler*<br/>
Планировщик, который будет использоваться для планирования задач.

*_PScheduleGroup*<br/>
Группа расписаний, которая будет использоваться для планирования задач.

## <a name="link_source"></a><a name="link_source"></a> link_source

Связывает указанный блок источника с этим `target_block` объектом.

```cpp
virtual void link_source(_Inout_ ISource<_Source_type>* _PSource);
```

### <a name="parameters"></a>Параметры

*_PSource*<br/>
Указатель на `ISource` блок, который должен быть связан.

### <a name="remarks"></a>Комментарии

Эта функция не должна вызываться напрямую для `target_block` объекта. Блоки должны быть соединены вместе с помощью `link_target` метода для `ISource` блоков, которые будут вызывать `link_source` метод для соответствующего целевого объекта.

## <a name="process_input_messages"></a><a name="process_input_messages"></a> process_input_messages

Обрабатывает сообщения, полученные как входные данные.

```cpp
virtual void process_input_messages(_Inout_ message<_Source_type>* _PMessage);
```

### <a name="parameters"></a>Параметры

*_PMessage*<br/>
Указатель на сообщение, которое должно быть обработано.

## <a name="process_message"></a><a name="process_message"></a> process_message

При переопределении в производном классе обрабатывает сообщение, которое ранее было принято данным объектом `target_block`.

```cpp
virtual void process_message(message<_Source_type> *);
```

## <a name="propagate"></a><a name="propagate"></a> распространения

Асинхронно передает сообщение из исходного блока в этот целевой блок.

```cpp
virtual message_status propagate(
    _Inout_opt_ message<_Source_type>* _PMessage,
    _Inout_opt_ ISource<_Source_type>* _PSource);
```

### <a name="parameters"></a>Параметры

*_PMessage*<br/>
Указатель на объект `message`.

*_PSource*<br/>
Указатель на исходный блок, предлагающий сообщение.

### <a name="return-value"></a>Возвращаемое значение

[Message_status](concurrency-namespace-enums.md) указывает, что цель решила делать с сообщением.

### <a name="remarks"></a>Комментарии

Метод вызывает исключение [invalid_argument](../../../standard-library/invalid-argument-class.md) , если `_PMessage` параметр или имеет значение `_PSource` `NULL` .

## <a name="propagate_message"></a><a name="propagate_message"></a> propagate_message

При переопределении в производном классе этот метод асинхронно передает сообщение из `ISource` блока в этот `target_block` объект. Он вызывается `propagate` методом при вызове из исходного блока.

```cpp
virtual message_status propagate_message(
    _Inout_ message<_Source_type>* _PMessage,
    _Inout_ ISource<_Source_type>* _PSource) = 0;
```

### <a name="parameters"></a>Параметры

*_PMessage*<br/>
Указатель на объект `message`.

*_PSource*<br/>
Указатель на исходный блок, предлагающий сообщение.

### <a name="return-value"></a>Возвращаемое значение

[Message_status](concurrency-namespace-enums.md) указывает, что цель решила делать с сообщением.

## <a name="register_filter"></a><a name="register_filter"></a> register_filter

Регистрирует метод фильтра, который будет вызываться для каждого полученного сообщения.

```cpp
void register_filter(filter_method const& _Filter);
```

### <a name="parameters"></a>Параметры

*_Filter*<br/>
Метод Filter.

## <a name="remove_sources"></a><a name="remove_sources"></a> remove_sources

Отменяет связь со всеми источниками после ожидания завершения ожидающих асинхронных операций отправки.

```cpp
void remove_sources();
```

### <a name="remarks"></a>Комментарии

Все целевые блоки должны вызывать эту подпрограммы для удаления источников в их деструкторе.

## <a name="send"></a><a name="send"></a> Отправить

Синхронно передает сообщение из исходного блока в этот целевой блок.

```cpp
virtual message_status send(
    _Inout_ message<_Source_type>* _PMessage,
    _Inout_ ISource<_Source_type>* _PSource);
```

### <a name="parameters"></a>Параметры

*_PMessage*<br/>
Указатель на объект `message`.

*_PSource*<br/>
Указатель на исходный блок, предлагающий сообщение.

### <a name="return-value"></a>Возвращаемое значение

[Message_status](concurrency-namespace-enums.md) указывает, что цель решила делать с сообщением.

### <a name="remarks"></a>Комментарии

Метод вызывает исключение [invalid_argument](../../../standard-library/invalid-argument-class.md) , если `_PMessage` параметр или имеет значение `_PSource` `NULL` .

Использование `send` метода за пределами инициации сообщений и распространения сообщений в сети опасно и может привести к взаимоблокировке.

Когда `send` метод возвращает значение, сообщение уже было принято и передано в целевой блок или было отклонено целевым объектом.

## <a name="send_message"></a><a name="send_message"></a> send_message

При переопределении в производном классе этот метод синхронно передает сообщение из `ISource` блока в этот `target_block` объект. Он вызывается `send` методом при вызове из исходного блока.

```cpp
virtual message_status send_message(
    _Inout_ message<_Source_type> *,
    _Inout_ ISource<_Source_type> *);
```

### <a name="return-value"></a>Возвращаемое значение

[Message_status](concurrency-namespace-enums.md) указывает, что цель решила делать с сообщением.

### <a name="remarks"></a>Комментарии

По умолчанию этот блок возвращается, `declined` если он не переопределен производным классом.

## <a name="sync_send"></a><a name="sync_send"></a> sync_send

Синхронная Отправка сообщения для обработки.

```cpp
void sync_send(_Inout_opt_ message<_Source_type>* _PMessage);
```

### <a name="parameters"></a>Параметры

*_PMessage*<br/>
Указатель на отправляемое сообщение.

## <a name="target_block"></a><a name="ctor"></a> target_block

Формирует объект `target_block`.

```cpp
target_block();
```

## <a name="target_block"></a><a name="dtor"></a> ~ target_block

Уничтожает `target_block` объект.

```cpp
virtual ~target_block();
```

## <a name="unlink_source"></a><a name="unlink_source"></a> unlink_source

Отменяет связь указанного исходного блока с этим `target_block` объектом.

```cpp
virtual void unlink_source(_Inout_ ISource<_Source_type>* _PSource);
```

### <a name="parameters"></a>Параметры

*_PSource*<br/>
Указатель на `ISource` блок, связь с которым необходимо отменить.

## <a name="unlink_sources"></a><a name="unlink_sources"></a> unlink_sources

Отменяет связь со всеми исходными блоками этого `target_block` объекта.

```cpp
virtual void unlink_sources();
```

## <a name="wait_for_async_sends"></a><a name="wait_for_async_sends"></a> wait_for_async_sends

Ожидает завершения всех асинхронных распространителей.

```cpp
void wait_for_async_sends();
```

### <a name="remarks"></a>Комментарии

Этот метод используется деструкторами блоков сообщений для обеспечения времени завершения всех асинхронных операций перед уничтожением блока.

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency](concurrency-namespace.md)<br/>
[Класс ITarget](itarget-class.md)
