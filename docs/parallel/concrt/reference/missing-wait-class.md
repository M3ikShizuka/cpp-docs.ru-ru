---
description: 'Дополнительные сведения о: missing_wait классе'
title: Класс missing_wait
ms.date: 11/04/2016
f1_keywords:
- missing_wait
- CONCRT/concurrency::missing_wait
- CONCRT/concurrency::missing_wait::missing_wait
helpviewer_keywords:
- missing_wait class
ms.assetid: ff981875-bd43-47e3-806f-b03c9f418b18
ms.openlocfilehash: bfbfdf4c2a52573d08c048bac278386aed1dc5a8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97202188"
---
# <a name="missing_wait-class"></a>Класс missing_wait

Этот класс описывает исключение, возникающее при наличии задач, для которых по-прежнему запланирован объект `task_group` или `structured_task_group` на момент выполнения деструктора объекта. Это исключение не создается, если деструктор достигается из-за освобождения стека в результате исключения.

## <a name="syntax"></a>Синтаксис

```cpp
class missing_wait : public std::exception;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[missing_wait](#ctor)|Перегружен. Формирует объект `missing_wait`.|

## <a name="remarks"></a>Комментарии

Отсутствие потока исключений. Вы несете ответственность за вызов `wait` метода или `run_and_wait` `task_group` `structured_task_group` объекта или перед тем, как разрешить этому объекту уничтожения. Среда выполнения создает это исключение в качестве свидетельства о том, что вы забыли вызвать `wait` `run_and_wait` метод или.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`exception`

`missing_wait`

## <a name="requirements"></a>Требования

**Заголовок:** ConcRT. h

**Пространство имен:** параллелизм

## <a name="missing_wait"></a><a name="ctor"></a> missing_wait

Формирует объект `missing_wait`.

```cpp
explicit _CRTIMP missing_wait(_In_z_ const char* _Message) throw();

missing_wait() throw();
```

### <a name="parameters"></a>Параметры

*_Message*<br/>
Описательное сообщение об ошибке.

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency](concurrency-namespace.md)<br/>
[Класс task_group](task-group-class.md)<br/>
[ожидания](task-group-class.md)<br/>
[run_and_wait](task-group-class.md)<br/>
[Класс structured_task_group](structured-task-group-class.md)
