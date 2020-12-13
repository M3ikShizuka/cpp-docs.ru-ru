---
description: 'Дополнительные сведения о: invalid_oversubscribe_operation классе'
title: Класс invalid_oversubscribe_operation
ms.date: 11/04/2016
f1_keywords:
- invalid_oversubscribe_operation
- CONCRT/concurrency::invalid_oversubscribe_operation
- CONCRT/concurrency::invalid_oversubscribe_operation::invalid_oversubscribe_operation
helpviewer_keywords:
- invalid_oversubscribe_operation class
ms.assetid: 0a9c5f08-d5e6-4ad0-90a9-517472b3ac28
ms.openlocfilehash: 435e3ce0eba29188711c51aa9253060fc08ac62c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97334527"
---
# <a name="invalid_oversubscribe_operation-class"></a>Класс invalid_oversubscribe_operation

Этот класс описывает исключение, возникающее при `Context::Oversubscribe` вызове метода с `_BeginOversubscription` параметром, для которого задано значение **`false`** без предварительного вызова метода, для `Context::Oversubscribe` которого `_BeginOversubscription` параметру задано значение **`true`** .

## <a name="syntax"></a>Синтаксис

```cpp
class invalid_oversubscribe_operation : public std::exception;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[invalid_oversubscribe_operation](#ctor)|Перегружен. Создает объект `invalid_oversubscribe_operation`.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`exception`

`invalid_oversubscribe_operation`

## <a name="requirements"></a>Требования

**Заголовок:** ConcRT. h

**Пространство имен:** параллелизм

## <a name="invalid_oversubscribe_operation"></a><a name="ctor"></a> invalid_oversubscribe_operation

Создает объект `invalid_oversubscribe_operation`.

```cpp
explicit _CRTIMP invalid_oversubscribe_operation(_In_z_ const char* _Message) throw();

invalid_oversubscribe_operation() throw();
```

### <a name="parameters"></a>Параметры

*_Message*<br/>
Описательное сообщение об ошибке.

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency](concurrency-namespace.md)
