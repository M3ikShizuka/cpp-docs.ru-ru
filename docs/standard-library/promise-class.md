---
description: Дополнительные сведения о классе Promise
title: Класс promise
ms.date: 10/18/2018
f1_keywords:
- future/std::promise
- future/std::promise::promise
- future/std::promise::get_future
- future/std::promise::set_exception
- future/std::promise::set_exception_at_thread_exit
- future/std::promise::set_value
- future/std::promise::set_value_at_thread_exit
- future/std::promise::swap
ms.assetid: 2931558c-d94a-4ba1-ac4f-20bf7b6e23f9
helpviewer_keywords:
- std::promise [C++]
- std::promise [C++], promise
- std::promise [C++], get_future
- std::promise [C++], set_exception
- std::promise [C++], set_exception_at_thread_exit
- std::promise [C++], set_value
- std::promise [C++], set_value_at_thread_exit
- std::promise [C++], swap
ms.openlocfilehash: bf65a3d1f42cb331c2e87ab418f2917947b0bed7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97340636"
---
# <a name="promise-class"></a>Класс promise

Описывает *асинхронный поставщик*.

## <a name="syntax"></a>Синтаксис

```cpp
template <class Ty>
class promise;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[обещан](#promise)|Формирует объект `promise`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[get_future](#get_future)|Возвращает [future](../standard-library/future-class.md), связанный с этим объектом promise.|
|[set_exception](#set_exception)|Атомарно устанавливает результат этого объекта promise для обозначения исключения.|
|[set_exception_at_thread_exit](#set_exception_at_thread_exit)|Атомарно устанавливает результат этого объекта promise для обозначения исключения и доставляет уведомление только после того, как все локальные объекты в текущем потоке уничтожены (обычно при выходе из потока).|
|[set_value](#set_value)|Атомарно устанавливает результат этого объекта promise для обозначения значения.|
|[set_value_at_thread_exit](#set_value_at_thread_exit)|Атомарно устанавливает результат этого объекта promise для обозначения значения и доставляет уведомление только после того, как все локальные объекты в текущем потоке уничтожены (обычно при выходе из потока).|
|[позиции](#swap)|Выполняет обмен *связанного асинхронного состояния* этого объекта promise с состоянием указанного объекта promise.|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[Promise:: operator =](#op_eq)|Назначение общего состояния этого объекта promise.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

*обещан*

## <a name="requirements"></a>Требования

**Заголовок:**\<future>

**Пространство имен:** std

## <a name="promiseget_future"></a><a name="get_future"></a> обещание:: get_future

Возвращает объект [future](../standard-library/future-class.md), который имеет то же самое *связанное асинхронное состояние*, что и данный объект promise.

```cpp
future<Ty> get_future();
```

### <a name="remarks"></a>Комментарии

Если объект promise пустой, этот метод выдает [future_error](../standard-library/future-error-class.md) с [error_code](../standard-library/error-code-class.md)`no_state`.

Если этот метод уже вызывался для объекта promise с тем же самым связанным асинхронным состоянием, метод выдает `future_error` с `error_code``future_already_retrieved`.

## <a name="promiseoperator"></a><a name="op_eq"></a> Promise:: operator =

Передает *связанное асинхронное состояние* от указанного объекта `promise`.

```cpp
promise& operator=(promise&& Other) noexcept;
```

### <a name="parameters"></a>Параметры

*Иной*\
Объект `promise`.

### <a name="return-value"></a>Возвращаемое значение

`*this`

### <a name="remarks"></a>Комментарии

Этот оператор передает связанное асинхронное состояние из *другого*. После перемещения значение *other* *пусто*.

## <a name="promisepromise-constructor"></a><a name="promise"></a> обещание: конструктор:p ромисе

Формирует объект `promise`.

```cpp
promise();
template <class Alloc>
promise(allocator_arg_t, const Alloc& Al);
promise(promise&& Other) noexcept;
```

### <a name="parameters"></a>Параметры

*Al*\
Распределитель памяти. [\<allocators>](../standard-library/allocators-header.md)Дополнительные сведения см. в разделе.

*Иной*\
Объект `promise`.

### <a name="remarks"></a>Комментарии

Первый конструктор создает *пустой* `promise` объект.

Второй конструктор конструирует пустой `promise` объект и использует *Al* для выделения памяти.

Третий конструктор конструирует `promise` объект и передает связанное асинхронное состояние из *другого* и оставляет *другой* пустой.

## <a name="promiseset_exception"></a><a name="set_exception"></a> обещание:: set_exception

Автоматически сохраняет исключение в качестве результата объекта `promise` и устанавливает *связанное асинхронное состояние* в значение *ready*.

```cpp
void set_exception(exception_ptr Exc);
```

### <a name="parameters"></a>Параметры

*Исключенного*\
[Exception_ptr](../standard-library/exception-typedefs.md#exception_ptr), который сохраняется этим методом как результат исключения.

### <a name="remarks"></a>Комментарии

Если объект `promise` не имеет связанного асинхронного состояния, этот метод выдает [future_error](../standard-library/future-error-class.md) с кодом ошибки `no_state`.

Если `set_exception`, [set_exception_at_thread_exit](#set_exception_at_thread_exit), [set_value](#set_value) или [set_value_at_thread_exit](#set_value_at_thread_exit) уже вызывались для объекта `promise`, который имеет то же самое связанное асинхронное состояние, то этот метод выдает `future_error` с кодом ошибки `promise_already_satisfied`.

В результате работы этого метода все потоки, которые заблокированы на связанном асинхронном состоянии, разблокируются.

## <a name="promiseset_exception_at_thread_exit"></a><a name="set_exception_at_thread_exit"></a> обещание:: set_exception_at_thread_exit

Атомарно устанавливает результат `promise` для указания исключения, доставляя уведомление только после того, как все локальные объекты в текущем потоке уничтожены (обычно при завершении потока).

```cpp
void set_exception_at_thread_exit(exception_ptr Exc);
```

### <a name="parameters"></a>Параметры

*Исключенного*\
[Exception_ptr](../standard-library/exception-typedefs.md#exception_ptr), который сохраняется этим методом как результат исключения.

### <a name="remarks"></a>Комментарии

Если объект promise не имеет *связанного асинхронного состояния*, этот метод выдает [future_error](../standard-library/future-error-class.md) с кодом ошибки `no_state`.

Если [set_exception](#set_exception), `set_exception_at_thread_exit` , [set_Value](#set_value)или [set_value_at_thread_exit](#set_value_at_thread_exit) уже вызван для `promise` объекта, который имеет то же связанное асинхронное состояние, этот метод создает исключение `future_error` , которое имеет код ошибки `promise_already_satisfied` .

В отличие от [set_exception](#set_exception) этот метод не устанавливает связанное асинхронное состояние в значение ready до тех пор, пока не будут уничтожены все локальные объекты в текущем потоке. Обычно потоки, которые заблокированы в связанном асинхронном состоянии, не разблокируются до завершения текущего потока.

## <a name="promiseset_value"></a><a name="set_value"></a> обещание:: set_value

Атомарно сохраняет значение в виде результата этого объекта `promise` и устанавливает *связанное асинхронное состояние* в значение *ready*.

```cpp
void promise::set_value(const Ty& Val);
void promise::set_value(Ty&& Val);
void promise<Ty&>::set_value(Ty& Val);
void promise<void>::set_value();
```

### <a name="parameters"></a>Параметры

*Val*\
Значение, которое будет сохранено в качестве результата.

### <a name="remarks"></a>Комментарии

Если объект `promise` не имеет связанного асинхронного состояния, этот метод выдает [future_error](../standard-library/future-error-class.md) с кодом ошибки `no_state`.

Если [set_exception](#set_exception), [set_exception_at_thread_exit](#set_exception_at_thread_exit)`set_value` или [set_value_at_thread_exit](#set_value_at_thread_exit) уже вызывались для объекта `promise`, имеющего то же самое связанное асинхронное состояние, то этот метод выдает `future_error` с кодом ошибки `promise_already_satisfied`.

В результате работы этого метода все потоки, которые заблокированы на связанном асинхронном состоянии, разблокируются.

Первый метод также создает исключение, возникающее при копировании *Val* в связанное асинхронное состояние. В этой ситуации связанное асинхронное состояние не устанавливается в значение ready.

Второй метод также создает исключение, возникающее при перемещении *Val* в связанное асинхронное состояние. В этой ситуации связанное асинхронное состояние не устанавливается в значение ready.

Для частичной специализации `promise<Ty&>` сохраненное значение действует как ссылка на *Val*.

Для специализации `promise<void>` сохраненные значения не существуют.

## <a name="promiseset_value_at_thread_exit"></a><a name="set_value_at_thread_exit"></a> обещание:: set_value_at_thread_exit

Атомарно сохраняет значение в качестве результата этого объекта `promise`.

```cpp
void promise::set_value_at_thread_exit(const Ty& Val);
void promise::set_value_at_thread_exit(Ty&& Val);
void promise<Ty&>::set_value_at_thread_exit(Ty& Val);
void promise<void>::set_value_at_thread_exit();
```

### <a name="parameters"></a>Параметры

*Val*\
Значение, которое будет сохранено в качестве результата.

### <a name="remarks"></a>Комментарии

Если объект promise не имеет *связанного асинхронного состояния*, этот метод выдает [future_error](../standard-library/future-error-class.md) с кодом ошибки `no_state`.

Если [set_exception](#set_exception), [set_exception_at_thread_exit](#set_exception_at_thread_exit), [set_value](#set_value) или `set_value_at_thread_exit` уже вызывались для объекта `promise`, имеющего то же самое связанное асинхронное состояние, этот метод выдает `future_error` с кодом ошибки `promise_already_satisfied`.

В отличие от `set_value` связанное асинхронное состояние не устанавливается в значение ready до тех пор, пока все локальные объекты текущего потока не будут уничтожены. Обычно потоки, которые заблокированы в связанном асинхронном состоянии, не разблокируются до завершения текущего потока.

Первый метод также создает исключение, возникающее при копировании *Val* в связанное асинхронное состояние.

Второй метод также создает исключение, возникающее при перемещении *Val* в связанное асинхронное состояние.

Для частичной специализации `promise<Ty&>` хранимое значение фактически является ссылкой на *Val*.

Для специализации `promise<void>` сохраненные значения не существуют.

## <a name="promiseswap"></a><a name="swap"></a> Promise:: swap

Обменивает *связанное асинхронное состояние* данного объекта promise с состоянием указанного объекта.

```cpp
void swap(promise& Other) noexcept;
```

### <a name="parameters"></a>Параметры

*Иной*\
Объект `promise`.

## <a name="see-also"></a>См. также раздел

[Справочник по файлам заголовков](../standard-library/cpp-standard-library-header-files.md)
