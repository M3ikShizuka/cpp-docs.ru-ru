---
description: 'Дополнительные сведения о: runtime_exception классе'
title: runtime_exception - класс
ms.date: 03/27/2019
f1_keywords:
- runtime_exception
- AMPRT/runtime_exception
- AMPRT/Concurrency::runtime_exception
- AMPRT/Concurrency::runtime_exception::get_error_code
helpviewer_keywords:
- runtime_exception class
ms.assetid: 8fe3ce2c-3d4c-4b9c-95e8-e592f37adefd
ms.openlocfilehash: 8fa5750473ee5a9b84255313832bbcbbba406394
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97329940"
---
# <a name="runtime_exception-class"></a>runtime_exception - класс

Базовый тип для исключений в библиотеке C++ Accelerated Massive Parallelism (AMP).

### <a name="syntax"></a>Синтаксис

```cpp
class runtime_exception : public std::exception;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Конструктор runtime_exception](#ctor)|Инициализирует новый экземпляр класса `runtime_exception`.|
|[Деструктор ~ runtime_exception](#dtor)|Уничтожает `runtime_exception` объект.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[get_error_code](#get_error_code)|Возвращает код ошибки, вызвавший исключение.|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[Оператор =](#operator_eq)|Копирует содержимое указанного `runtime_exception` объекта в этот объект.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`exception`

`runtime_exception`

## <a name="requirements"></a>Требования

**Заголовок:** ампрт. h

**Пространство имен** : Concurrency

## <a name="runtime_exception-constructor"></a><a name="ctor"></a> Конструктор runtime_exception

Инициализирует новый экземпляр класса.

### <a name="syntax"></a>Синтаксис

```cpp
runtime_exception(
    const char * _Message,
    HRESULT _Hresult ) throw();

explicit runtime_exception(
    HRESULT _Hresult ) throw();

runtime_exception(
    const runtime_exception & _Other ) throw();
```

### <a name="parameters"></a>Параметры

*_Message*<br/>
Описание ошибки, вызвавшей исключение.

*_Hresult*<br/>
Значение HRESULT ошибки, вызвавшее исключение.

*_Other*<br/>
Копируемый объект `runtime_exception`.

### <a name="return-value"></a>Возвращаемое значение

Объект `runtime_exception`.

## <a name="runtime_exception-destructor"></a><a name="dtor"></a>  Деструктор ~ runtime_exception

Уничтожает объект.

### <a name="syntax"></a>Синтаксис

```cpp
virtual ~runtime_exception() throw();
```

## <a name="get_error_code"></a><a name="get_error_code"></a> get_error_code

Возвращает код ошибки, вызвавший исключение.

### <a name="syntax"></a>Синтаксис

```cpp
HRESULT get_error_code() const throw();
```

### <a name="return-value"></a>Возвращаемое значение

Значение HRESULT ошибки, вызвавшее исключение.

## <a name="operator"></a><a name="operator_eq"></a> Оператор =

Копирует содержимое указанного `runtime_exception` объекта в этот объект.

### <a name="syntax"></a>Синтаксис

```cpp
runtime_exception & operator= (    const runtime_exception & _Other ) throw();
```

### <a name="parameters"></a>Параметры

*_Other*<br/>
Копируемый объект `runtime_exception`.

### <a name="return-value"></a>Возвращаемое значение

Ссылка на этот `runtime_exception` объект.

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency (C++ AMP)](concurrency-namespace-cpp-amp.md)
