---
description: 'Дополнительные сведения о: invalid_operation классе'
title: Класс invalid_operation
ms.date: 11/04/2016
f1_keywords:
- invalid_operation
- CONCRT/concurrency::invalid_operation
- CONCRT/concurrency::invalid_operation::invalid_operation
helpviewer_keywords:
- invalid_operation class
ms.assetid: 26ba07dc-fcdf-44cb-b748-a31d35205b52
ms.openlocfilehash: f3050d487f2c374f66f264b6e568fce5244d25ba
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97334539"
---
# <a name="invalid_operation-class"></a>Класс invalid_operation

Данный класс описывает исключение, возникающее при выполнении недопустимой операции, которая не описывается более точно другим типом исключения, создаваемым средой выполнения с параллелизмом.

## <a name="syntax"></a>Синтаксис

```cpp
class invalid_operation : public std::exception;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[invalid_operation](#ctor)|Перегружен. Создает объект `invalid_operation`.|

## <a name="remarks"></a>Комментарии

Различные методы, создающие это исключение, обычно документируют, в каких обстоятельствах они создают его.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`exception`

`invalid_operation`

## <a name="requirements"></a>Требования

**Заголовок:** ConcRT. h

**Пространство имен:** параллелизм

## <a name="invalid_operation"></a><a name="ctor"></a> invalid_operation

Создает объект `invalid_operation`.

```cpp
explicit _CRTIMP invalid_operation(_In_z_ const char* _Message) throw();

invalid_operation() throw();
```

### <a name="parameters"></a>Параметры

*_Message*<br/>
Описательное сообщение об ошибке.

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency](concurrency-namespace.md)
