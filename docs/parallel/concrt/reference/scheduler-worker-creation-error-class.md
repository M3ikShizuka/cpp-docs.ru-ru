---
description: 'Дополнительные сведения о: scheduler_worker_creation_error классе'
title: Класс scheduler_worker_creation_error
ms.date: 11/04/2016
f1_keywords:
- scheduler_worker_creation_error
- CONCRT/concurrency::scheduler_worker_creation_error
- CONCRT/concurrency::scheduler_worker_creation_error::scheduler_worker_creation_error
helpviewer_keywords:
- scheduler_worker_creation_error class
ms.assetid: 4aec1c3e-c32a-41b2-899d-2d898f23b3c7
ms.openlocfilehash: f0fbb0aed19738bb88e4cbfe3a72580627c4fca9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97188720"
---
# <a name="scheduler_worker_creation_error-class"></a>Класс scheduler_worker_creation_error

Этот класс описывает исключение, которое создается из-за сбоя создания рабочего контекста выполнения в исполняющей среде с параллелизмом.

## <a name="syntax"></a>Синтаксис

```cpp
class scheduler_worker_creation_error : public scheduler_resource_allocation_error;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[scheduler_worker_creation_error](#ctor)|Перегружен. Формирует объект `scheduler_worker_creation_error`.|

## <a name="remarks"></a>Комментарии

Это исключение обычно создается при сбое вызова, адресованного операционной системе, для создания контекста выполнения из исполняющей среды с параллелизмом. Контексты выполнения — это потоки, которые выполняют задачи исполняющей среды с параллелизмом. Код ошибки, который обычно возвращается из вызова метода Win32 `GetLastError`, преобразуется в значение типа `HRESULT` и может быть получен посредством метода базового класса `get_error_code`.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`exception`

[scheduler_resource_allocation_error](scheduler-resource-allocation-error-class.md)

`scheduler_worker_creation_error`

## <a name="requirements"></a>Требования

**Заголовок:** ConcRT. h

**Пространство имен:** параллелизм

## <a name="scheduler_worker_creation_error"></a><a name="ctor"></a> scheduler_worker_creation_error

Формирует объект `scheduler_worker_creation_error`.

```cpp
scheduler_worker_creation_error(
    _In_z_ const char* _Message,
    HRESULT _Hresult) throw();

explicit _CRTIMP scheduler_worker_creation_error(
    HRESULT _Hresult) throw();
```

### <a name="parameters"></a>Параметры

*_Message*<br/>
Описательное сообщение об ошибке.

*_Hresult*<br/>
`HRESULT`Значение ошибки, вызвавшей исключение.

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency](concurrency-namespace.md)
