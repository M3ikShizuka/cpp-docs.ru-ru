---
description: 'Дополнительные сведения о: invalid_scheduler_policy_value классе'
title: Класс invalid_scheduler_policy_value
ms.date: 11/04/2016
f1_keywords:
- concrt/concurrency::invalid_scheduler_policy_value
helpviewer_keywords:
- invalid_scheduler_policy_value class
ms.assetid: 8c533e3f-2774-4192-8616-b2313b859bf7
ms.openlocfilehash: c91295646b0bc85ea4ed5ee8f376c1ed029e4f0a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97334491"
---
# <a name="invalid_scheduler_policy_value-class"></a>Класс invalid_scheduler_policy_value

Этот класс описывает исключение, создаваемое, когда ключу политики объекта `SchedulerPolicy` присваивается недопустимое для этого ключа значение.

## <a name="syntax"></a>Синтаксис

```cpp
class invalid_scheduler_policy_value : public std::exception;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[invalid_scheduler_policy_value] (недопустимый параметр-Scheduler-Policy-Thread-спецификация-Class. md # ctor|Перегружен. Создает объект `invalid_scheduler_policy_value`.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`exception`

`invalid_scheduler_policy_value`

## <a name="requirements"></a>Требования

**Заголовок:** ConcRT. h

**Пространство имен:** параллелизм

## <a name="invalid_scheduler_policy_value"></a><a name="ctor"></a> invalid_scheduler_policy_value

Создает объект `invalid_scheduler_policy_value`.

```cpp
explicit _CRTIMP invalid_scheduler_policy_value(_In_z_ const char* _Message) throw();

invalid_scheduler_policy_value() throw();
```

### <a name="parameters"></a>Параметры

*_Message*<br/>
Описательное сообщение об ошибке.

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency](concurrency-namespace.md)<br/>
[Класс SchedulerPolicy](schedulerpolicy-class.md)
