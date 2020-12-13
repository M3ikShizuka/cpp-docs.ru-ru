---
description: 'Дополнительные сведения о: mem_fun_t классе'
title: Класс mem_fun_t
ms.date: 02/21/2019
f1_keywords:
- functional/std::mem_fun_t
helpviewer_keywords:
- mem_fun_t class
ms.assetid: 242566d4-750c-4c87-9d63-2e2c9d19ca2a
ms.openlocfilehash: 53c3103c8f2c855d8d6ff9a2861ace4f2c69c787
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97149153"
---
# <a name="mem_fun_t-class"></a>Класс mem_fun_t

Класс адаптера, который позволяет `non_const` вызывать функцию-член, которая не принимает аргументов, как объект унарной функции при инициализации с помощью аргумента указателя. Не рекомендуется использовать в C++ 11, удалено в C++ 17.

## <a name="syntax"></a>Синтаксис

```cpp
template <class Result, class Type>
class mem_fun_t : public unary_function<Type *, Result> {
    explicit mem_fun_t(Result (Type::* _Pm)());

    Result operator()(Type* _Pleft) const;
};
```

### <a name="parameters"></a>Параметры

*_Pm*\
Указатель на функцию-член класса `Type` для преобразования в объект функции.

*_Pleft*\
Объект, для которого вызывается функция-член *_Pm* .

## <a name="return-value"></a>Возвращаемое значение

Адаптируемая унарная функция.

## <a name="remarks"></a>Комментарии

Шаблон класса хранит копию *_Pm*, которая должна быть указателем на функцию-член класса `Type` в закрытом объекте-члене. Он определяет свою функцию `operator()` -член как возвращающую ( `_Pleft` ->*  `_Pm` ) ().

## <a name="example"></a>Пример

Конструктор `mem_fun_t` обычно не используется напрямую; для адаптации функций-членов используется вспомогательная функция `mem_fun`. Пример использования адаптера функции-члена см. в разделе [mem_fun](../standard-library/functional-functions.md#mem_fun).
