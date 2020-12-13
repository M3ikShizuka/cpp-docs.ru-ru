---
description: 'Дополнительные сведения о: invalid_multiple_scheduling классе'
title: Класс invalid_multiple_scheduling
ms.date: 11/04/2016
f1_keywords:
- invalid_multiple_scheduling
- CONCRT/concurrency::invalid_multiple_scheduling
- CONCRT/concurrency::invalid_multiple_scheduling::invalid_multiple_scheduling
helpviewer_keywords:
- invalid_multiple_scheduling class
ms.assetid: e9a47cb7-a778-4df7-92b0-3752119fd4c7
ms.openlocfilehash: 23d89d93c953a3c01a6e0e698cfa7489effd2986
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97334558"
---
# <a name="invalid_multiple_scheduling-class"></a>Класс invalid_multiple_scheduling

Этот класс описывает исключение, создаваемое, если объект `task_handle` запланирован несколько раз с помощью метода `run` объекта `task_group` или `structured_task_group` без промежуточных вызовов любого из методов `wait` или `run_and_wait`.

## <a name="syntax"></a>Синтаксис

```cpp
class invalid_multiple_scheduling : public std::exception;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[invalid_multiple_scheduling](#ctor)|Перегружен. Создает объект `invalid_multiple_scheduling`.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`exception`

`invalid_multiple_scheduling`

## <a name="requirements"></a>Требования

**Заголовок:** ConcRT. h

**Пространство имен:** параллелизм

## <a name="invalid_multiple_scheduling"></a><a name="ctor"></a> invalid_multiple_scheduling

Создает объект `invalid_multiple_scheduling`.

```cpp
explicit _CRTIMP invalid_multiple_scheduling(_In_z_ const char* _Message) throw();

invalid_multiple_scheduling() throw();
```

### <a name="parameters"></a>Параметры

*_Message*<br/>
Описательное сообщение об ошибке.

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency](concurrency-namespace.md)<br/>
[Класс task_handle](task-handle-class.md)<br/>
[Класс task_group](task-group-class.md)<br/>
[запуска](task-group-class.md)<br/>
[ожидания](task-group-class.md)<br/>
[run_and_wait](task-group-class.md)<br/>
[Класс structured_task_group](structured-task-group-class.md)
