---
description: 'Дополнительные сведения о: is_placeholder классе'
title: Класс is_placeholder
ms.date: 11/04/2016
f1_keywords:
- functional/std::is_placeholder
helpviewer_keywords:
- is_placeholder class
ms.assetid: 2b21a792-96d1-4bb8-b911-0db796510835
ms.openlocfilehash: 84d73da6ffe2446a8448b0ff5f30604d259493b1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97230657"
---
# <a name="is_placeholder-class"></a>Класс is_placeholder

Проверяет, является ли тип заполнителем.

## <a name="syntax"></a>Синтаксис

Структура is_placeholder {статическое константное значение int;};

## <a name="remarks"></a>Комментарии

Значение константы `value` равно 0, если тип `Ty` не является заполнителем. В противном случае значение — это положение аргумента вызова функции, к которому он привязывается. Используется для определения значения `N` n-ного заполнителя `_N`.

## <a name="example"></a>Пример

```cpp
// std__functional__is_placeholder.cpp
// compile with: /EHsc
#include <functional>
#include <iostream>

using namespace std::placeholders;

template<class Expr>
void test_for_placeholder(const Expr&)
{
    std::cout << std::is_placeholder<Expr>::value << std::endl;
}

int main()
{
    test_for_placeholder(3.0);
    test_for_placeholder(_3);

    return (0);
}
```

```Output
0
3
```
