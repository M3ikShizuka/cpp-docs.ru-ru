---
description: 'Дополнительные сведения о: improper_lock классе'
title: Класс improper_lock
ms.date: 11/04/2016
f1_keywords:
- improper_lock
- CONCRT/concurrency::improper_lock
- CONCRT/concurrency::improper_lock::improper_lock
helpviewer_keywords:
- improper_lock class
ms.assetid: 8f494942-7748-4a2a-8de2-23414bfe6346
ms.openlocfilehash: 8e29172ad171bbd3f95b3079840fb50b91dfe577
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97334643"
---
# <a name="improper_lock-class"></a>Класс improper_lock

Этот класс описывает исключение, создаваемое, когда блокировка получена неправильно.

## <a name="syntax"></a>Синтаксис

```cpp
class improper_lock : public std::exception;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[improper_lock](#ctor)|Перегружен. Создает элемент `improper_lock exception`.|

## <a name="remarks"></a>Комментарии

Как правило, это исключение возникает при попытке получить блокировку, не допускающую повторного входа, рекурсивно в том же контексте.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`exception`

`improper_lock`

## <a name="requirements"></a>Требования

**Заголовок:** ConcRT. h

**Пространство имен:** параллелизм

## <a name="improper_lock"></a><a name="ctor"></a> improper_lock

Создает элемент `improper_lock exception`.

```cpp
explicit _CRTIMP improper_lock(_In_z_ const char* _Message) throw();

improper_lock() throw();
```

### <a name="parameters"></a>Параметры

*_Message*<br/>
Описательное сообщение об ошибке.

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency](concurrency-namespace.md)<br/>
[Класс critical_section](critical-section-class.md)<br/>
[Класс reader_writer_lock](reader-writer-lock-class.md)
