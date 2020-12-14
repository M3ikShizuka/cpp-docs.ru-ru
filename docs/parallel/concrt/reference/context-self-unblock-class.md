---
description: 'Дополнительные сведения о: context_self_unblock классе'
title: Класс context_self_unblock
ms.date: 11/04/2016
f1_keywords:
- context_self_unblock
- CONCRT/concurrency::context_self_unblock
- CONCRT/concurrency::context_self_unblock::context_self_unblock
helpviewer_keywords:
- context_self_unblock class
ms.assetid: 9601cd28-4f40-4c2e-89ab-747068956331
ms.openlocfilehash: 51fae67530e2836b92a6ab7a13e2b136f1d438c9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97188980"
---
# <a name="context_self_unblock-class"></a>Класс context_self_unblock

Этот класс описывает исключение, которое создается при вызове метода `Unblock` объекта `Context` из того же контекста. Это означает попытку данного контекста разблокировать самого себя.

## <a name="syntax"></a>Синтаксис

```cpp
class context_self_unblock : public std::exception;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[context_self_unblock](#ctor)|Перегружен. Формирует объект `context_self_unblock`.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`exception`

`context_self_unblock`

## <a name="requirements"></a>Требования

**Заголовок:** ConcRT. h

**Пространство имен:** параллелизм

## <a name="context_self_unblock"></a><a name="ctor"></a> context_self_unblock

Формирует объект `context_self_unblock`.

```cpp
explicit _CRTIMP context_self_unblock(_In_z_ const char* _Message) throw();

context_self_unblock() throw();
```

### <a name="parameters"></a>Параметры

*_Message*<br/>
Описательное сообщение об ошибке.

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency](concurrency-namespace.md)
