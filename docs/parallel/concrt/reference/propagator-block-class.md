---
description: 'Дополнительные сведения о: propagator_block классе'
title: Класс propagator_block
ms.date: 11/04/2016
f1_keywords:
- propagator_block
- AGENTS/concurrency::propagator_block
- AGENTS/concurrency::propagator_block::propagator_block
- AGENTS/concurrency::propagator_block::propagate
- AGENTS/concurrency::propagator_block::send
- AGENTS/concurrency::propagator_block::decline_incoming_messages
- AGENTS/concurrency::propagator_block::initialize_source_and_target
- AGENTS/concurrency::propagator_block::link_source
- AGENTS/concurrency::propagator_block::process_input_messages
- AGENTS/concurrency::propagator_block::propagate_message
- AGENTS/concurrency::propagator_block::register_filter
- AGENTS/concurrency::propagator_block::remove_network_links
- AGENTS/concurrency::propagator_block::send_message
- AGENTS/concurrency::propagator_block::unlink_source
- AGENTS/concurrency::propagator_block::unlink_sources
helpviewer_keywords:
- propagator_block class
ms.assetid: 86aa75fd-eda5-42aa-aadf-25c0c1c9742d
ms.openlocfilehash: 4dd006829e01f663be20be76a2cc2e0364ef7b38
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97115291"
---
# <a name="propagator_block-class"></a>Класс propagator_block

Класс `propagator_block` — это абстрактный базовый класс для блоков сообщений, которые являются одновременно блоками источников и целевыми блоками. Он объединяет функциональные возможности обоих классов, `source_block` и `target_block`.

## <a name="syntax"></a>Синтаксис

```cpp
template<class _TargetLinkRegistry, class _SourceLinkRegistry, class _MessageProcessorType = ordered_message_processor<typename _TargetLinkRegistry::type::type>>
class propagator_block : public source_block<_TargetLinkRegistry,
    _MessageProcessorType>,
public ITarget<typename _SourceLinkRegistry::type::source_type>;
```

### <a name="parameters"></a>Параметры

*_TargetLinkRegistry*<br/>
Реестр ссылок, используемый для хранения целевых ссылок.

*_SourceLinkRegistry*<br/>
Реестр ссылок, используемый для хранения исходных ссылок.

*_MessageProcessorType*<br/>
Тип процессора для обработки сообщений.

## <a name="members"></a>Элементы

### <a name="public-typedefs"></a>Общедоступные определения типов

|Имя|Описание|
|----------|-----------------|
|`source_iterator`|Тип итератора для `source_link_manager` этого объекта `propagator_block` .|

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[propagator_block](#ctor)|Формирует объект `propagator_block`.|
|[Деструктор ~ propagator_block](#dtor)|Уничтожает объект `propagator_block` .|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[распространения](#propagate)|Асинхронно передает сообщение из исходного блока в этот целевой блок.|
|[send](#send)|Синхронно инициирует сообщение для этого блока. Вызывается `ISource` блоком. По завершении этой функции сообщение уже будет распространено в блок.|

### <a name="protected-methods"></a>Защищенные методы

|Имя|Описание|
|----------|-----------------|
|[decline_incoming_messages](#decline_incoming_messages)|Указывает блоку, что следует отклонять новые сообщения.|
|[initialize_source_and_target](#initialize_source_and_target)|Инициализирует базовый объект. В частности, необходимо `message_processor` инициализировать объект.|
|[link_source](#link_source)|Связывает указанный блок источника с этим `propagator_block` объектом.|
|[process_input_messages](#process_input_messages)|Обработка входных сообщений. Это полезно только для блоков распространения, которые являются производными от source_block (переопределяет [source_block::p rocess_input_messages](source-block-class.md#process_input_messages).)|
|[propagate_message](#propagate_message)|При переопределении в производном классе этот метод асинхронно передает сообщение из `ISource` блока в этот `propagator_block` объект. Он вызывается `propagate` методом при вызове из исходного блока.|
|[register_filter](#register_filter)|Регистрирует метод фильтра, который будет вызываться для каждого полученного сообщения.|
|[remove_network_links](#remove_network_links)|Удаляет все связи исходной и целевой сетей из этого `propagator_block` объекта.|
|[send_message](#send_message)|При переопределении в производном классе этот метод синхронно передает сообщение из `ISource` блока в этот `propagator_block` объект. Он вызывается `send` методом при вызове из исходного блока.|
|[unlink_source](#unlink_source)|Отменяет связь указанного исходного блока с этим `propagator_block` объектом.|
|[unlink_sources](#unlink_sources)|Отменяет связь со всеми исходными блоками этого `propagator_block` объекта. (Переопределяет метод [ITarget:: unlink_sources](itarget-class.md#unlink_sources).)|

## <a name="remarks"></a>Комментарии

Чтобы избежать множественного наследования, `propagator_block` класс наследует от `source_block` класса и `ITarget` абстрактного класса. Большая часть функциональных возможностей в `target_block` классе реплицируется здесь.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[ISource](isource-class.md)

[ITarget](itarget-class.md)

[source_block](source-block-class.md)

`propagator_block`

## <a name="requirements"></a>Требования

**Заголовок:** agents.h

**Пространство имен:** параллелизм

## <a name="decline_incoming_messages"></a><a name="decline_incoming_messages"></a> decline_incoming_messages

Указывает блоку, что следует отклонять новые сообщения.

```cpp
void decline_incoming_messages();
```

### <a name="remarks"></a>Комментарии

Этот метод вызывается деструктором, чтобы гарантировать отклонение новых сообщений в процессе уничтожения.

## <a name="initialize_source_and_target"></a><a name="initialize_source_and_target"></a> initialize_source_and_target

Инициализирует базовый объект. В частности, необходимо `message_processor` инициализировать объект.

```cpp
void initialize_source_and_target(
    _Inout_opt_ Scheduler* _PScheduler = NULL,
    _Inout_opt_ ScheduleGroup* _PScheduleGroup = NULL);
```

### <a name="parameters"></a>Параметры

*_PScheduler*<br/>
Планировщик, который будет использоваться для планирования задач.

*_PScheduleGroup*<br/>
Группа расписаний, которая будет использоваться для планирования задач.

## <a name="link_source"></a><a name="link_source"></a> link_source

Связывает указанный блок источника с этим `propagator_block` объектом.

```cpp
virtual void link_source(_Inout_ ISource<_Source_type>* _PSource);
```

### <a name="parameters"></a>Параметры

*_PSource*<br/>
Указатель на `ISource` блок, который должен быть связан.

## <a name="process_input_messages"></a><a name="process_input_messages"></a> process_input_messages

Обработка входных сообщений. Подходит только для блоков распространения, производных от source_block.

```cpp
virtual void process_input_messages(_Inout_ message<_Target_type>* _PMessage);
```

### <a name="parameters"></a>Параметры

*_PMessage*<br/>
Указатель на сообщение, которое должно быть обработано.

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

`propagate`Метод вызывается в целевом блоке с помощью связанного исходного блока. Она помещает в очередь асинхронную задачу для работы с сообщением, если она еще не находится в очереди или не исполняется.

Метод вызывает исключение [invalid_argument](../../../standard-library/invalid-argument-class.md) , если `_PMessage` параметр или имеет значение `_PSource` `NULL` .

## <a name="propagate_message"></a><a name="propagate_message"></a> propagate_message

При переопределении в производном классе этот метод асинхронно передает сообщение из `ISource` блока в этот `propagator_block` объект. Он вызывается `propagate` методом при вызове из исходного блока.

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

## <a name="propagator_block"></a><a name="ctor"></a> propagator_block

Формирует объект `propagator_block`.

```cpp
propagator_block();
```

## <a name="propagator_block"></a><a name="dtor"></a> ~ propagator_block

Уничтожает объект `propagator_block` .

```cpp
virtual ~propagator_block();
```

## <a name="register_filter"></a><a name="register_filter"></a> register_filter

Регистрирует метод фильтра, который будет вызываться для каждого полученного сообщения.

```cpp
void register_filter(filter_method const& _Filter);
```

### <a name="parameters"></a>Параметры

*_Filter*<br/>
Метод Filter.

## <a name="remove_network_links"></a><a name="remove_network_links"></a> remove_network_links

Удаляет все связи исходной и целевой сетей из этого `propagator_block` объекта.

```cpp
void remove_network_links();
```

## <a name="send"></a><a name="send"></a> Отправить

Синхронно инициирует сообщение для этого блока. Вызывается `ISource` блоком. По завершении этой функции сообщение уже будет распространено в блок.

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

Этот метод вызывает исключение [invalid_argument](../../../standard-library/invalid-argument-class.md) , если `_PMessage` `_PSource` параметр или имеет значение `NULL` .

## <a name="send_message"></a><a name="send_message"></a> send_message

При переопределении в производном классе этот метод синхронно передает сообщение из `ISource` блока в этот `propagator_block` объект. Он вызывается `send` методом при вызове из исходного блока.

```cpp
virtual message_status send_message(
    _Inout_ message<_Source_type> *,
    _Inout_ ISource<_Source_type> *);
```

### <a name="return-value"></a>Возвращаемое значение

[Message_status](concurrency-namespace-enums.md) указывает, что цель решила делать с сообщением.

### <a name="remarks"></a>Комментарии

По умолчанию этот блок возвращается, `declined` если он не переопределен производным классом.

## <a name="unlink_source"></a><a name="unlink_source"></a> unlink_source

Отменяет связь указанного исходного блока с этим `propagator_block` объектом.

```cpp
virtual void unlink_source(_Inout_ ISource<_Source_type>* _PSource);
```

### <a name="parameters"></a>Параметры

*_PSource*<br/>
Указатель на `ISource` блок, связь с которым необходимо отменить.

## <a name="unlink_sources"></a><a name="unlink_sources"></a> unlink_sources

Отменяет связь со всеми исходными блоками этого `propagator_block` объекта.

```cpp
virtual void unlink_sources();
```

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency](concurrency-namespace.md)<br/>
[Класс source_block](source-block-class.md)<br/>
[Класс ITarget](itarget-class.md)
