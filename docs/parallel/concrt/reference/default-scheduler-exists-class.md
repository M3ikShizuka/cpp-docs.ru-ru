---
description: 'Дополнительные сведения о: default_scheduler_exists классе'
title: Класс default_scheduler_exists
ms.date: 11/04/2016
f1_keywords:
- default_scheduler_exists
- CONCRT/concurrency::default_scheduler_exists
- CONCRT/concurrency::default_scheduler_exists::default_scheduler_exists
helpviewer_keywords:
- default_scheduler_exists class
ms.assetid: f6e575e2-4e0f-455a-9e06-54f462ce0c1c
ms.openlocfilehash: 6921f7bd820271cf590707c2e56cefa9f576cefe
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97284854"
---
# <a name="default_scheduler_exists-class"></a>Класс default_scheduler_exists

Этот класс описывает исключение, возникающее при вызове метода `Scheduler::SetDefaultSchedulerPolicy`, когда планировщик по умолчанию уже существует в процессе.

## <a name="syntax"></a>Синтаксис

```cpp
class default_scheduler_exists : public std::exception;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[default_scheduler_exists](#ctor)|Перегружен. Формирует объект `default_scheduler_exists`.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`exception`

`default_scheduler_exists`

## <a name="requirements"></a>Требования

**Заголовок:** ConcRT. h

**Пространство имен:** параллелизм

## <a name="default_scheduler_exists"></a><a name="ctor"></a> default_scheduler_exists

Формирует объект `default_scheduler_exists`.

```cpp
explicit _CRTIMP default_scheduler_exists(_In_z_ const char* _Message) throw();

default_scheduler_exists() throw();
```

### <a name="parameters"></a>Параметры

*_Message*<br/>
Описательное сообщение об ошибке.

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency](concurrency-namespace.md)
