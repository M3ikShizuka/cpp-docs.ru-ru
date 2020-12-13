---
description: 'Дополнительные сведения о: mem_fun1_t классе'
title: Класс mem_fun1_t
ms.date: 02/21/2019
f1_keywords:
- functional/std::mem_fun1_t
helpviewer_keywords:
- mem_fun1_t class
ms.assetid: 01a8c2c2-b2f7-4e3f-869c-5b5b9f06ea54
ms.openlocfilehash: a0fd8f060757c7dc5004ad753fd168c9e644e1b8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97149088"
---
# <a name="mem_fun1_t-class"></a>Класс mem_fun1_t

Класс адаптера, который позволяет `non_const` вызывать функцию-член, которая принимает один аргумент, как объект бинарной функции при инициализации с помощью аргумента указателя. Не рекомендуется использовать в C++ 11, удалено в C++ 17.

## <a name="syntax"></a>Синтаксис

```cpp
template <class Result, class Type, class Arg>
class mem_fun1_t : public binary_function<Type *, Arg, Result> {
    explicit mem_fun1_t(
    Result (Type::* _Pm)(Arg));

    Result operator()(
    Type* _Pleft,
    Arg right) const;
};
```

### <a name="parameters"></a>Параметры

*_Pm*\
Указатель на функцию-член класса `Type` для преобразования в объект функции.

*_Pleft*\
Объект, для которого вызывается функция-член *_Pm* .

*Правильно*\
Аргумент, присваиваемый *_Pm*.

## <a name="return-value"></a>Возвращаемое значение

Адаптируемая бинарная функция.

## <a name="remarks"></a>Комментарии

Шаблон класса хранит копию *_Pm*, которая должна быть указателем на функцию-член класса `Type` в закрытом объекте-члене. Он определяет свою функцию `operator()` -член как возвращающую (**_Pleft** -> \* `_Pm` ) (**right**).

## <a name="example"></a>Пример

Конструктор `mem_fun1_t` обычно не используется напрямую; для адаптации функций-членов используется вспомогательная функция `mem_fun`. Пример использования адаптера функции-члена см. в разделе [mem_fun](../standard-library/functional-functions.md#mem_fun).
