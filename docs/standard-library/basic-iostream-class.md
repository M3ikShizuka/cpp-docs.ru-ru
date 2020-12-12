---
description: 'Дополнительные сведения о: basic_iostream классе'
title: Класс basic_iostream
ms.date: 11/04/2016
f1_keywords:
- istream/std::basic_iostream
- istream/std::basic_iostream::swap
helpviewer_keywords:
- basic_iostream class
ms.assetid: 294b680b-eb49-4066-8db2-6d52dac9d6e3
ms.openlocfilehash: c9b605c5eb36a0bc725ce21e2c89617357078d40
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97321518"
---
# <a name="basic_iostream-class"></a>Класс basic_iostream

Класс потока, поддерживающий ввод и вывод.

## <a name="syntax"></a>Синтаксис

```cpp
template <class Elem, class Tr = char_traits<Elem>>
class basic_iostream : public basic_istream<Elem, Tr>,
    public basic_ostream<Elem, Tr>
{
public:
    explicit basic_iostream(basic_streambuf<Elem, Tr>* strbuf);

    virtual ~basic_iostream();

};
```

## <a name="remarks"></a>Remarks

Шаблон класса описывает объект, управляющий вставками с помощью базового класса [basic_ostream](../standard-library/basic-ostream-class.md) <  `Elem` , `Tr`> и извлечений через его базовый класс [basic_istream](../standard-library/basic-istream-class.md) <  `Elem` `Tr`>. Два объекта совместно используют общий виртуальный базовый класс [basic_ios](../standard-library/basic-ios-class.md) <  `Elem` , `Tr`>. Они также управляют общим буфером потока с элементами типа `Elem`, признаки символов которых определяются классом `Tr`. Конструктор инициализирует базовые классы с помощью `basic_istream`( **strbuf**) и `basic_ostream`( **strbuf**).

### <a name="constructors"></a>Конструкторы

|Конструктор|Описание|
|-|-|
|[basic_iostream](#basic_iostream)|Создание объекта `basic_iostream`.|

### <a name="member-functions"></a>Функции элементов

|Функция-член|Описание|
|-|-|
|[позиции](#swap)|Меняет местами содержимое предоставленного объекта `basic_iostream` на содержимое этого объекта.|

### <a name="operators"></a>Операторы

|Оператор|Описание|
|-|-|
|[Оператор =](#op_eq)|Присваивает значение указанного объекта `basic_iostream` этому объекту. Это назначение перемещения, включающее `rvalue`, которое не оставляет копию.|

## <a name="requirements"></a>Требования

**Заголовок:**\<istream>

**Пространство имен:** std

## <a name="basic_iostreambasic_iostream"></a><a name="basic_iostream"></a> basic_iostream:: basic_iostream

Создание объекта `basic_iostream`.

```cpp
explicit basic_iostream(basic_streambuf<Elem, Tr>* strbuf);

basic_iostream(basic_iostream&& right);

basic_iostream();
```

### <a name="parameters"></a>Параметры

*strBuf*\
Существующий объект `basic_streambuf`.

*Правильно*\
Существующий объект `basic_iostream`, который используется для создания нового объекта `basic_iostream`.

### <a name="remarks"></a>Комментарии

Первый конструктор инициализирует базовые объекты посредством `basic_istream(strbuf)` и `basic_ostream(strbuf)`.

Второй конструктор инициализирует базовые объекты путем вызова `move(right)` .

## <a name="basic_iostreamoperator"></a><a name="op_eq"></a> basic_iostream:: operator =

Присваивает значение указанного объекта `basic_iostream` этому объекту. Это назначение перемещения, включающее rvalue, которое не оставляет копию.

```cpp
basic_iostream& operator=(basic_iostream&& right);
```

### <a name="parameters"></a>Параметры

*Правильно*\
Ссылка `rvalue` на объект `basic_iostream`, на основе которого будет присвоено значение.

### <a name="remarks"></a>Комментарии

Оператор члена вызывает `swap(right)` .

## <a name="basic_iostreamswap"></a><a name="swap"></a> basic_iostream:: swap

Меняет местами содержимое предоставленного объекта `basic_iostream` на содержимое этого объекта.

```cpp
void swap(basic_iostream& right);
```

### <a name="parameters"></a>Параметры

*Правильно*\
Объект `basic_iostream` для обмена.

### <a name="remarks"></a>Комментарии

Функция члена вызывает `swap(right)` .

## <a name="see-also"></a>См. также раздел

[Безопасность потоков в стандартной библиотеке C++](../standard-library/thread-safety-in-the-cpp-standard-library.md)\
[Программирование iostream](../standard-library/iostream-programming.md)\
[Соглашения iostream](../standard-library/iostreams-conventions.md)
