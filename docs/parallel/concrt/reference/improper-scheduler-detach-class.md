---
description: 'Дополнительные сведения о: improper_scheduler_detach классе'
title: Класс improper_scheduler_detach
ms.date: 11/04/2016
f1_keywords:
- improper_scheduler_detach
- CONCRT/concurrency::improper_scheduler_detach
- CONCRT/concurrency::improper_scheduler_detach::improper_scheduler_detach
helpviewer_keywords:
- improper_scheduler_detach class
ms.assetid: 30132102-c900-4951-a470-b63b4e3aa2d2
ms.openlocfilehash: 62def23a4a3459c4cb8268b3b0f4df4a77025668
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97334612"
---
# <a name="improper_scheduler_detach-class"></a>Класс improper_scheduler_detach

Этот класс описывает исключение, создаваемое при вызове метода `CurrentScheduler::Detach` в контексте, который не присоединен ни к одному планировщику с помощью метода `Attach` объекта `Scheduler`.

## <a name="syntax"></a>Синтаксис

```cpp
class improper_scheduler_detach : public std::exception;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[improper_scheduler_detach](#ctor)|Перегружен. Создает объект `improper_scheduler_detach`.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`exception`

`improper_scheduler_detach`

## <a name="requirements"></a>Требования

**Заголовок:** ConcRT. h

**Пространство имен:** параллелизм

## <a name="improper_scheduler_detach"></a><a name="ctor"></a> improper_scheduler_detach

Создает объект `improper_scheduler_detach`.

```cpp
explicit _CRTIMP improper_scheduler_detach(_In_z_ const char* _Message) throw();

improper_scheduler_detach() throw();
```

### <a name="parameters"></a>Параметры

*_Message*<br/>
Описательное сообщение об ошибке.

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency](concurrency-namespace.md)<br/>
[Класс Scheduler](scheduler-class.md)
