---
description: 'Дополнительные сведения о: bad_target классе'
title: Класс bad_target
ms.date: 11/04/2016
f1_keywords:
- bad_target
- CONCRT/concurrency::bad_target
- CONCRT/concurrency::bad_target::bad_target
helpviewer_keywords:
- bad_target class
ms.assetid: e6dcddbf-9217-4fac-ac7f-7b8b4781d2f5
ms.openlocfilehash: 0bade57ef06ee1ecf675d69531da918fc2a3510f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97172249"
---
# <a name="bad_target-class"></a>Класс bad_target

Этот класс описывает исключение, которое создается, если блок обмена сообщениями получает указатель на целевой объект, который неверен для выполняемой операции.

## <a name="syntax"></a>Синтаксис

```cpp
class bad_target : public std::exception;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[bad_target](#ctor)|Перегружен. Формирует объект `bad_target`.|

## <a name="remarks"></a>Комментарии

Это исключение обычно вызывается по таким причинам, как цель пытается использовать сообщение, которое зарезервировано для другого целевого объекта или освобождения резервирования, которое не удерживается.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`exception`

`bad_target`

## <a name="requirements"></a>Требования

**Заголовок:** ConcRT. h

**Пространство имен:** параллелизм

## <a name="bad_target"></a><a name="ctor"></a> bad_target

Формирует объект `bad_target`.

```cpp
explicit _CRTIMP bad_target(_In_z_ const char* _Message) throw();

bad_target() throw();
```

### <a name="parameters"></a>Параметры

*_Message*<br/>
Описательное сообщение об ошибке.

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency](concurrency-namespace.md)<br/>
[Асинхронные блоки сообщений](../../../parallel/concrt/asynchronous-message-blocks.md)
