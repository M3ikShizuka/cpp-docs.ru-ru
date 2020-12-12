---
description: 'Дополнительные сведения о: is_bind_expression классе'
title: Класс is_bind_expression
ms.date: 11/04/2016
f1_keywords:
- functional/std::is_bind_expression
helpviewer_keywords:
- is_bind_expression class
ms.assetid: 0715f9e9-2239-4778-a1cf-2c21f49dfd47
ms.openlocfilehash: 1430beefd1c046b2910c562385f26d2788c88865
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97323850"
---
# <a name="is_bind_expression-class"></a>Класс is_bind_expression

Проверяет, что тип создается путем вызова `bind`.

## <a name="syntax"></a>Синтаксис

```cpp
template<class Ty>
struct is_bind_expression {
   static const bool value;
};
```

## <a name="remarks"></a>Remarks

Член константы `value` имеет значение true, если тип `Ty` — это тип, возвращаемый вызовом метода `bind`, в противном случае — значение false.

## <a name="example"></a>Пример

```cpp
// std__functional__is_bind_expression.cpp
// compile with: /EHsc
#include <functional>
#include <iostream>

void square(double x)
{
    std::cout << x << "^2 == " << x * x << std::endl;
}

template<class Expr>
void test_for_bind(const Expr&)
{
    std::cout << std::is_bind_expression<Expr>::value << std::endl;
}

int main()
{
    test_for_bind(3.0 * 3.0);
    test_for_bind(std::bind(square, 3));

    return (0);
}
```

```Output
0
1
```
