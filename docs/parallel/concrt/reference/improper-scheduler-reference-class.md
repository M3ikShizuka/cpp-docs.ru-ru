---
description: 'Дополнительные сведения о: improper_scheduler_reference классе'
title: Класс improper_scheduler_reference
ms.date: 11/04/2016
f1_keywords:
- improper_scheduler_reference
- CONCRT/concurrency::improper_scheduler_reference
- CONCRT/concurrency::improper_scheduler_reference::improper_scheduler_reference
helpviewer_keywords:
- improper_scheduler_reference class
ms.assetid: 434a7512-7796-4255-92a7-f3bf71c6a7a7
ms.openlocfilehash: 4857418e14908b2d085d52249236d6395284b98a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97334604"
---
# <a name="improper_scheduler_reference-class"></a>Класс improper_scheduler_reference

Данный класс описывает исключение, которое создается при вызове метода `Reference` на объекте `Scheduler`, который завершает работу, из контекста, который не является частью этого планировщика.

## <a name="syntax"></a>Синтаксис

```cpp
class improper_scheduler_reference : public std::exception;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[improper_scheduler_reference](#ctor)|Перегружен. Создает объект `improper_scheduler_reference`.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`exception`

`improper_scheduler_reference`

## <a name="requirements"></a>Требования

**Заголовок:** ConcRT. h

**Пространство имен:** параллелизм

## <a name="improper_scheduler_reference"></a><a name="ctor"></a> improper_scheduler_reference

Создает объект `improper_scheduler_reference`.

```cpp
explicit _CRTIMP improper_scheduler_reference(_In_z_ const char* _Message) throw();

improper_scheduler_reference() throw();
```

### <a name="parameters"></a>Параметры

*_Message*<br/>
Описательное сообщение об ошибке.

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency](concurrency-namespace.md)<br/>
[Класс Scheduler](scheduler-class.md)
