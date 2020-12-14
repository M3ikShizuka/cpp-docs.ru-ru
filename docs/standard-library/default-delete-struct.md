---
description: 'Дополнительные сведения о: default_delete struct'
title: Структура default_delete
ms.date: 04/04/2019
f1_keywords:
- memory/std::default_delete
helpviewer_keywords:
- default_delete struct
ms.openlocfilehash: 5b7d652dbb556957acf96ba63ac9ce14b628fb7e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97232971"
---
# <a name="default_delete-struct"></a>Структура default_delete

Стандартный объект функции, который выполняет операцию деления ( `operator/` ) в своих аргументах.

## <a name="syntax"></a>Синтаксис

```cpp
template <class T>
    struct default_delete
```

## <a name="requirements"></a>Требования

**Заголовок:**\<memory>

**Пространство имен:** std

## <a name="members"></a>Члены

### <a name="constructors"></a>Конструкторы

|Имя|Описание|
|-|-|
|[default_delete](#default_delete)|Конструктор для объектов типа `default_delete`.|

### <a name="operators"></a>Операторы

|Имя|Описание|
|-|-|
|[оператор ()](#op_paren)|Ссылочный оператор для доступа `default_delete` .|

## <a name="default_delete"></a><a name="default_delete"></a> default_delete

Конструктор для объектов типа `default_delete`.

```cpp
constexpr default_delete() noexcept = default;
template <class U>
    default_delete(const default_delete<U>&) noexcept;
```

## <a name="operator"></a><a name="op_paren"></a> оператор ()

Ссылочный оператор для доступа `default_delete` .

```cpp
void operator()(T*) const;
```

## <a name="see-also"></a>См. также раздел

[\<memory>](../standard-library/memory.md)
