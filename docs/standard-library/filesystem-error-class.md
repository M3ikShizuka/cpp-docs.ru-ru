---
description: 'Дополнительные сведения о: filesystem_error классе'
title: Класс filesystem_error
ms.date: 09/10/2018
f1_keywords:
- filesystem/std::experimental::filesystem::filesystem_error
ms.assetid: c53aac27-c1fa-43e4-8967-48ea8ba1f172
ms.openlocfilehash: 8165bfbc0d59dbbdab17d910e2e2f7973988049d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97232438"
---
# <a name="filesystem_error-class"></a>Класс filesystem_error

Базовый класс для всех исключений, создаваемых для отчета о переполнении системы низкого уровня.

## <a name="syntax"></a>Синтаксис

```cpp
class filesystem_error    : public system_error;
```

## <a name="remarks"></a>Remarks

Класс выступает в качестве базового класса для всех исключений, порождаемых для сообщения об ошибке в \<filesystem> функциях. Он сохраняет объект типа `string` , который вызывается `mymesg` здесь в целях демонстрации. Он также хранит два объекта типа `path` , называемые `mypval1` и `mypval2` .

## <a name="members"></a>Члены

### <a name="constructors"></a>Конструкторы

|Имя|Описание|
|-|-|
|[filesystem_error](#filesystem_error)|Конструирует `filesystem_error` сообщение.|

### <a name="functions"></a>Функции

|Имя|Описание|
|-|-|
|[path1](#path1)|Возвращает `mypval1`.|
|[path2](#path2)|Возвращает `mypval2`.|
|[What](#what)|Возвращает указатель на `NTBS`.|

## <a name="requirements"></a>Требования

**Заголовок:**\<filesystem>

**Пространство имен:** std::experimental::filesystem

## <a name="filesystem_error"></a><a name="filesystem_error"></a> filesystem_error

Первый конструктор конструирует свое сообщение от *what_arg* и *EC*. Второй конструктор также формирует свое сообщение из *Pval1*, которое хранится в `mypval1` . Третий конструктор также формирует свое сообщение из *Pval1*, которое хранится в `mypval1` , и из *Pval2*, который он хранит в `mypval2` .

```cpp
filesystem_error(const string& what_arg,
    error_code ec);

filesystem_error(const string& what_arg,
    const path& pval1,
    error_code ec);

filesystem_error(const string& what_arg,
    const path& pval1,
    const path& pval2,
    error_code ec);
```

### <a name="parameters"></a>Параметры

*what_arg*\
Указанное сообщение.

*контроллер*\
Указанный код ошибки.

*mypval1*\
Дополнительный указанный параметр сообщения.

*mypval2*\
Дополнительный указанный параметр сообщения.

## <a name="path1"></a><a name="path1"></a> path1

Функция-член возвращает значение `mypval1`.

```cpp
const path& path1() const noexcept;
```

## <a name="path2"></a><a name="path2"></a> path2

Функция-член возвращает значение `mypval2`.

```cpp
const path& path2() const noexcept;
```

## <a name="what"></a><a name="what"></a> What

Функция-член возвращает указатель на `NTBS` , желательно состоящий из `runtime_error::what()` , `system_error::what()` , `mymesg` , `mypval1.native_string()` и `mypval2.native_string()` .

```cpp
const char *what() const noexcept;
```
