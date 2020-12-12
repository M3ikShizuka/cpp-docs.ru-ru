---
description: 'Дополнительные сведения: &lt; функциональные &gt; операторы'
title: Операторы &lt;functional&gt;
ms.date: 11/04/2016
f1_keywords:
- functional/std::operator!=
- functional/std::operator==
helpviewer_keywords:
- functional operators
ms.assetid: d4b3c760-f3e2-4b65-bdaa-d42e8dd6f5e1
ms.openlocfilehash: a22e9203e89c041d5ed1925d55d1cd3aa6d61ba3
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97324243"
---
# <a name="ltfunctionalgt-operators"></a>Операторы &lt;functional&gt;

## <a name="operator"></a><a name="op_eq_eq"></a> Оператор = =

Проверяет, является ли вызываемый объект пустым.

```cpp
template <class Fty>
    bool operator==(const function<Fty>& f, null_ptr_type npc);

template <class Fty>
    bool operator==(null_ptr_type npc, const function<Fty>& f);
```

### <a name="parameters"></a>Параметры

*фти*\
Тип функции для заключения в оболочку.

*ж*\
Объект функции

*нпк*\
Указатель null

### <a name="remarks"></a>Комментарии

Операторы принимают аргумент, являющийся ссылкой на объект `function`, и аргумент, являющийся константой указателя null. В обоих случаях возвращается значение true только в том случае, если объект `function` пуст.

### <a name="example"></a>Пример

```cpp
// std__functional__operator_eq.cpp
// compile with: /EHsc
#include <functional>
#include <iostream>

int neg(int val)
{
    return (-val);
}

int main()
{
    std::function<int(int)> fn0;
    std::cout << std::boolalpha << "empty == "
        << (fn0 == 0) << std::endl;

    std::function<int(int)> fn1(neg);
    std::cout << std::boolalpha << "empty == "
        << (fn1 == 0) << std::endl;

    return (0);
}
```

```Output
empty == true
empty == false
```

## <a name="operator"></a><a name="op_neq"></a> operator! =

Проверяет, является ли вызываемый объект не пустым.

```cpp
template <class Fty>
    bool operator!=(const function<Fty>& f, null_ptr_type npc);

template <class Fty>
    bool operator!=(null_ptr_type npc, const function<Fty>& f);
```

### <a name="parameters"></a>Параметры

*фти*\
Тип функции для заключения в оболочку.

*ж*\
Объект функции

*нпк*\
Указатель null

### <a name="remarks"></a>Комментарии

Операторы принимают аргумент, являющийся ссылкой на объект `function`, и аргумент, являющийся константой указателя null. В обоих случаях возвращается значение true только в том случае, если объект `function` не пуст.

### <a name="example"></a>Пример

```cpp
// std__functional__operator_ne.cpp
// compile with: /EHsc
#include <functional>
#include <iostream>

int neg(int val)
    {
    return (-val);
    }

int main()
    {
    std::function<int (int)> fn0;
    std::cout << std::boolalpha << "not empty == "
        << (fn0 != 0) << std::endl;

    std::function<int (int)> fn1(neg);
    std::cout << std::boolalpha << "not empty == "
        << (fn1 != 0) << std::endl;

    return (0);
    }
```

```Output
not empty == false
not empty == true
```
