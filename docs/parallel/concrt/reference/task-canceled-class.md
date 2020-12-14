---
description: 'Дополнительные сведения о: task_canceled классе'
title: Класс task_canceled
ms.date: 11/04/2016
f1_keywords:
- task_canceled
- CONCRT/concurrency::task_canceled
- CONCRT/concurrency::task_canceled::task_canceled
helpviewer_keywords:
- task_canceled class
ms.assetid: c3f0b234-2cc1-435f-a48e-995f45b190be
ms.openlocfilehash: 223a1168464e312c272f770247b3574311ff97ed
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97188408"
---
# <a name="task_canceled-class"></a>Класс task_canceled

Этот класс описывает исключение, которое создается уровнем задач PPL для принудительной отмены текущей задачи. Он также вызывается `get()` методом в [задаче](/visualstudio/extensibility/debugger/task-class-internal-members)для отмененной задачи.

## <a name="syntax"></a>Синтаксис

```cpp
class task_canceled : public std::exception;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[task_canceled](#ctor)|Перегружен. Формирует объект `task_canceled`.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`exception`

`task_canceled`

## <a name="requirements"></a>Требования

**Заголовок:** ConcRT. h

**Пространство имен:** параллелизм

## <a name="task_canceled"></a><a name="ctor"></a> task_canceled

Формирует объект `task_canceled`.

```cpp
explicit _CRTIMP task_canceled(_In_z_ const char* _Message) throw();

task_canceled() throw();
```

### <a name="parameters"></a>Параметры

*_Message*<br/>
Описательное сообщение об ошибке.

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency](concurrency-namespace.md)
