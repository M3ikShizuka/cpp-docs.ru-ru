---
description: 'Дополнительные сведения о: improper_scheduler_attach классе'
title: Класс improper_scheduler_attach
ms.date: 11/04/2016
f1_keywords:
- improper_scheduler_attach
- CONCRT/concurrency::improper_scheduler_attach
- CONCRT/concurrency::improper_scheduler_attach::improper_scheduler_attach
helpviewer_keywords:
- improper_scheduler_attach class
ms.assetid: 5a76da0a-091b-4748-8f62-b3a28f674f9e
ms.openlocfilehash: 755cd72d20eb88dbd1ff7c58586f0aaf3b964a6a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97334622"
---
# <a name="improper_scheduler_attach-class"></a>Класс improper_scheduler_attach

Этот класс описывает исключение, которое создается при вызове метода `Attach` на объекте `Scheduler`, который уже присоединен к текущему контексту.

## <a name="syntax"></a>Синтаксис

```cpp
class improper_scheduler_attach : public std::exception;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[improper_scheduler_attach](#ctor)|Перегружен. Создает объект `improper_scheduler_attach`.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`exception`

`improper_scheduler_attach`

## <a name="requirements"></a>Требования

**Заголовок:** ConcRT. h

**Пространство имен:** параллелизм

## <a name="improper_scheduler_attach"></a><a name="ctor"></a> improper_scheduler_attach

Создает объект `improper_scheduler_attach`.

```cpp
explicit _CRTIMP improper_scheduler_attach(_In_z_ const char* _Message) throw();

improper_scheduler_attach() throw();
```

### <a name="parameters"></a>Параметры

*_Message*<br/>
Описательное сообщение об ошибке.

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency](concurrency-namespace.md)<br/>
[Класс Scheduler](scheduler-class.md)
