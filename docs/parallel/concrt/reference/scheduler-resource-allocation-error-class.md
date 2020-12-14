---
description: 'Дополнительные сведения о: scheduler_resource_allocation_error классе'
title: Класс scheduler_resource_allocation_error
ms.date: 11/04/2016
f1_keywords:
- scheduler_resource_allocation_error
- CONCRT/concurrency::scheduler_resource_allocation_error
- CONCRT/concurrency::scheduler_resource_allocation_error::scheduler_resource_allocation_error
- CONCRT/concurrency::scheduler_resource_allocation_error::get_error_code
helpviewer_keywords:
- scheduler_resource_allocation_error class
ms.assetid: 8b40449a-7abb-4d0a-bb85-c0e9a495ae97
ms.openlocfilehash: 50f84cbf76d30a415e2393797baa7d6cfa1e89f9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97188733"
---
# <a name="scheduler_resource_allocation_error-class"></a>Класс scheduler_resource_allocation_error

Этот класс описывает исключение, возникающее из-за сбоя получения критического ресурса в исполняющей среде с параллелизмом.

## <a name="syntax"></a>Синтаксис

```cpp
class scheduler_resource_allocation_error : public std::exception;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[scheduler_resource_allocation_error](#ctor)|Перегружен. Формирует объект `scheduler_resource_allocation_error`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[get_error_code](#get_error_code)|Возвращает код ошибки, вызвавший исключение.|

## <a name="remarks"></a>Комментарии

Это исключение обычно возникает при сбое вызова операционной системы из среда выполнения с параллелизмом. Код ошибки, который обычно возвращается из вызова метода Win32 `GetLastError`, преобразуется в значение типа `HRESULT` и может быть получен посредством метода `get_error_code`.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`exception`

`scheduler_resource_allocation_error`

## <a name="requirements"></a>Требования

**Заголовок:** ConcRT. h

**Пространство имен:** параллелизм

## <a name="get_error_code"></a><a name="get_error_code"></a> get_error_code

Возвращает код ошибки, вызвавший исключение.

```cpp
HRESULT get_error_code() const throw();
```

### <a name="return-value"></a>Возвращаемое значение

`HRESULT`Значение ошибки, вызвавшей исключение.

## <a name="scheduler_resource_allocation_error"></a><a name="ctor"></a> scheduler_resource_allocation_error

Формирует объект `scheduler_resource_allocation_error`.

```cpp
scheduler_resource_allocation_error(
    _In_z_ const char* _Message,
    HRESULT _Hresult) throw();

explicit _CRTIMP scheduler_resource_allocation_error(
    HRESULT _Hresult) throw();
```

### <a name="parameters"></a>Параметры

*_Message*<br/>
Описательное сообщение об ошибке.

*_Hresult*<br/>
`HRESULT`Значение ошибки, вызвавшей исключение.

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency](concurrency-namespace.md)
