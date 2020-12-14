---
description: 'Дополнительные сведения о: context_unblock_unbalanced классе'
title: Класс context_unblock_unbalanced
ms.date: 11/04/2016
f1_keywords:
- context_unblock_unbalanced
- CONCRT/concurrency::context_unblock_unbalanced
- CONCRT/concurrency::context_unblock_unbalanced::context_unblock_unbalanced
helpviewer_keywords:
- context_unblock_unbalanced class
ms.assetid: a76066c8-19dd-44fa-959a-6941ec1b0d2d
ms.openlocfilehash: d262ff52a675935f95664d2f7ddd69aa159aa0bc
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97188967"
---
# <a name="context_unblock_unbalanced-class"></a>Класс context_unblock_unbalanced

Данный класс описывает исключение, создаваемое, если вызовы методов `Block` и `Unblock` объекта `Context` объединены неправильно.

## <a name="syntax"></a>Синтаксис

```cpp
class context_unblock_unbalanced : public std::exception;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[context_unblock_unbalanced](#ctor)|Перегружен. Формирует объект `context_unblock_unbalanced`.|

## <a name="remarks"></a>Комментарии

Вызовы `Block` `Unblock` методов и `Context` объекта должны всегда быть парными. Среда выполнения с параллелизмом позволяет операциям выполняться в любом порядке. Например, за вызовом `Block` может следовать вызов `Unblock`, или наоборот. Это исключение возникает, если, например, два вызова `Unblock` метода были сделаны в строке на `Context` объекте, который не был заблокирован.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`exception`

`context_unblock_unbalanced`

## <a name="requirements"></a>Требования

**Заголовок:** ConcRT. h

**Пространство имен:** параллелизм

## <a name="context_unblock_unbalanced"></a><a name="ctor"></a> context_unblock_unbalanced

Формирует объект `context_unblock_unbalanced`.

```cpp
explicit _CRTIMP context_unblock_unbalanced(_In_z_ const char* _Message) throw();

context_unblock_unbalanced() throw();
```

### <a name="parameters"></a>Параметры

*_Message*<br/>
Описательное сообщение об ошибке.

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency](concurrency-namespace.md)
