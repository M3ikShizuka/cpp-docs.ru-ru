---
description: 'Дополнительные сведения о: operation_timed_out классе'
title: Класс operation_timed_out
ms.date: 11/04/2016
f1_keywords:
- operation_timed_out
- CONCRT/concurrency::operation_timed_out
- CONCRT/concurrency::operation_timed_out::operation_timed_out
helpviewer_keywords:
- operation_timed_out class
ms.assetid: 963efe1d-a6e0-477c-9a70-d93d8412c897
ms.openlocfilehash: 476dfc2d7f29b2769c076ff525f3d0eb1e20a8f5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97236559"
---
# <a name="operation_timed_out-class"></a>Класс operation_timed_out

Этот класс описывает исключение, создаваемое по истечении времени ожидания операции.

## <a name="syntax"></a>Синтаксис

```cpp
class operation_timed_out : public std::exception;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[operation_timed_out](#ctor)|Перегружен. Создает объект `operation_timed_out`.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`exception`

`operation_timed_out`

## <a name="requirements"></a>Требования

**Заголовок:** ConcRT. h

**Пространство имен:** параллелизм

## <a name="operation_timed_out"></a><a name="ctor"></a> operation_timed_out

Создает объект `operation_timed_out`.

```cpp
explicit _CRTIMP operation_timed_out(_In_z_ const char* _Message) throw();

operation_timed_out() throw();
```

### <a name="parameters"></a>Параметры

*_Message*<br/>
Описательное сообщение об ошибке.

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency](concurrency-namespace.md)
