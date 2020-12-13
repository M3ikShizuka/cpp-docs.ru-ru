---
description: 'Дополнительные сведения о: invalid_link_target классе'
title: Класс invalid_link_target
ms.date: 11/04/2016
f1_keywords:
- invalid_link_target
- CONCRT/concurrency::invalid_link_target
- CONCRT/concurrency::invalid_link_target::invalid_link_target
helpviewer_keywords:
- invalid_link_target class
ms.assetid: 33b64885-34d8-4d4e-a893-02e9f19c958e
ms.openlocfilehash: d080886c3aab0ecc120d4ce13f5f75f2eecfea8f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97334593"
---
# <a name="invalid_link_target-class"></a>Класс invalid_link_target

Данный класс описывает исключение, создаваемое, когда вызывается метод `link_target` блока обмена сообщениями и блок сообщений не может создать связь с целевым объектом. Это может быть результатом превышения числа ссылок, допустимых для блока сообщений, или попытки связать указанную цель с одним и тем же источником дважды.

## <a name="syntax"></a>Синтаксис

```cpp
class invalid_link_target : public std::exception;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[invalid_link_target](#ctor)|Перегружен. Создает объект `invalid_link_target`.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`exception`

`invalid_link_target`

## <a name="requirements"></a>Требования

**Заголовок:** ConcRT. h

**Пространство имен:** параллелизм

## <a name="invalid_link_target"></a><a name="ctor"></a> invalid_link_target

Создает объект `invalid_link_target`.

```cpp
explicit _CRTIMP invalid_link_target(_In_z_ const char* _Message) throw();

invalid_link_target() throw();
```

### <a name="parameters"></a>Параметры

*_Message*<br/>
Описательное сообщение об ошибке.

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency](concurrency-namespace.md)<br/>
[Асинхронные блоки сообщений](../../../parallel/concrt/asynchronous-message-blocks.md)
