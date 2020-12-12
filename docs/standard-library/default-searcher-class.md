---
description: 'Дополнительные сведения о: default_searcher классе'
title: класс default_searcher
ms.date: 08/03/2019
f1_keywords:
- functional/std::default_searcher
helpviewer_keywords:
- std::default_searcher [C++]
ms.openlocfilehash: 0eb47d3f4c49c9bb6c9c4e68ab2164b87ea9834d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97324592"
---
# <a name="default_searcher-class"></a>Класс default_searcher

`default_searcher`— Это тип объекта функции для операций, которые выполняют поиск последовательности, указанной в конструкторе объекта. Поиск выполняется в другой последовательности, предоставленной оператору вызова функции объекта. `default_searcher`Вызывает метод [std:: Search](algorithm-functions.md#search) для выполнения поиска.

## <a name="syntax"></a>Синтаксис

```cpp
template <class ForwardIterator, class BinaryPredicate = equal_to<>>
class default_searcher
{
    default_searcher(
        ForwardIterator pat_first,
        ForwardIterator pat_last,
        BinaryPredicate pred = BinaryPredicate());

    template <class ForwardIterator2>
    pair<ForwardIterator2, ForwardIterator2> operator()(
        ForwardIterator2 first,
        ForwardIterator2 last) const;
};
```

## <a name="members"></a>Члены

| Член | Описание |
| - | - |
| **Конструктор** | |
| [default_searcher](#default-searcher-constructor) | Конструирует экземпляр службы поиска. |
| **Операторы** | |
| [оператор ()](#operator-call) | Вызывает операцию в последовательности. |

## <a name="default_searcher-constructor"></a><a name="default-searcher-constructor"></a> Конструктор default_searcher

Конструирует `default_searcher` объект функции с помощью последовательности для поиска и предиката равенства.

```cpp
default_searcher(                   // C++17
    ForwardIterator pat_first,
    ForwardIterator pat_last,
    BinaryPredicate pred = BinaryPredicate());

constexpr default_searcher(         // C++20
    ForwardIterator pat_first,
    ForwardIterator pat_last,
    BinaryPredicate pred = BinaryPredicate());
```

### <a name="parameters"></a>Параметры

*pat_first*\
Начальный элемент последовательности для поиска.

*pat_last*\
Конец последовательности для поиска.

*Возможен*\
Необязательный предикат сравнения равенства для элементов последовательности. Если тип сравнения на равенство не указан, по умолчанию используется значение `std::equal_to` .

### <a name="remarks"></a>Комментарии

Создает исключение, созданное конструктором копий типов *бинарипредикате* или *ForwardIterator* .

Этот класс впервые появились в C++ 17. В c++ 20 создан конструктор **`constexpr`** .

## <a name="operator"></a><a name="operator-call"></a> оператор ()

Оператор Call оператора Function. Ищет в последовательности аргументов `[first, last)` последовательность, указанную в конструкторе.

```cpp
template <class ForwardIterator2>   // C++17
pair<ForwardIterator2, ForwardIterator2> operator()(
    ForwardIterator2 first,
    ForwardIterator2 last) const;

template <class ForwardIterator2>   // C++20
constexpr pair<ForwardIterator2, ForwardIterator2> operator()(
    ForwardIterator2 first,
    ForwardIterator2 last) const;
```

### <a name="parameters"></a>Параметры

*началь*\
Начальный элемент последовательности, в которой необходимо выполнить поиск.

*Последняя*\
Конец последовательности, в которой необходимо выполнить поиск.

### <a name="remarks"></a>Комментарии

Возвращает пару итераторов. Начальный итератор, который *я принимаю* , — это эффективный результат:

`std::search( first, last, pat_first, pat_last, pred )`.

Второй итератор пары *Last* , если *i** является *последним*. В противном случае это эффективный результат:

`std::next( i, std::distance( pat_first, pat_last ))`.

Этот класс впервые появились в C++ 17. В c++ 20 был создан оператор Call **`constexpr`** .

## <a name="see-also"></a>См. также раздел

[\<functional>](functional.md)\
[функции алгоритма](algorithm-functions.md)\
[std:: Search](algorithm-functions.md#search)
