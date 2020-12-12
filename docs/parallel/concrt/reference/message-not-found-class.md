---
description: 'Дополнительные сведения о: message_not_found классе'
title: Класс message_not_found
ms.date: 11/04/2016
f1_keywords:
- message_not_found
- CONCRT/concurrency::message_not_found
- CONCRT/concurrency::message_not_found::message_not_found
helpviewer_keywords:
- message_not_found class
ms.assetid: a96b9995-5ad7-4600-83c8-c15e329ff10e
ms.openlocfilehash: c0b098a530768617b2fa2cf52dfe374dc44a2c12
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97169389"
---
# <a name="message_not_found-class"></a>Класс message_not_found

Этот класс описывает исключение, создаваемое, когда блок обмена сообщениями не может найти запрошенное сообщение.

## <a name="syntax"></a>Синтаксис

```cpp
class message_not_found : public std::exception;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[message_not_found](#ctor)|Перегружен. Формирует объект `message_not_found`.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`exception`

`message_not_found`

## <a name="requirements"></a>Требования

**Заголовок:** ConcRT. h

**Пространство имен:** параллелизм

## <a name="message_not_found"></a><a name="ctor"></a> message_not_found

Формирует объект `message_not_found`.

```cpp
explicit _CRTIMP message_not_found(_In_z_ const char* _Message) throw();

message_not_found() throw();
```

### <a name="parameters"></a>Параметры

*_Message*<br/>
Описательное сообщение об ошибке.

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency](concurrency-namespace.md)<br/>
[Асинхронные блоки сообщений](../../../parallel/concrt/asynchronous-message-blocks.md)
