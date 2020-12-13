---
description: 'Дополнительные сведения: __Func__'
title: __func__
ms.date: 10/19/2017
f1_keywords:
- __func__
ms.assetid: a5299b8d-f0ee-4af2-91dd-8fb165e68798
ms.openlocfilehash: 6e075d0f566bb8c3eb72e62a30a36ef80528647b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97337709"
---
# <a name="__func__"></a>__func__

**(C++ 11)** Предопределенный идентификатор &#95;&#95;Func&#95;&#95; неявно определяется как строка, содержащая неполное и недекорированное имя включающей функции. &#95;&#95;Func&#95;&#95; задается стандартом C++ и не является расширением Microsoft.

## <a name="syntax"></a>Синтаксис

```cpp
__func__
```

## <a name="return-value"></a>Возвращаемое значение

Возвращает константный массив символов, заканчивающийся нулем, содержащий имя функции.

## <a name="example"></a>Пример

```cpp
#include <string>
#include <iostream>

namespace Test
{
    struct Foo
    {
        static void DoSomething(int i, std::string s)
        {
           std::cout << __func__ << std::endl; // Output: DoSomething
        }
    };
}

int main()
{
    Test::Foo::DoSomething(42, "Hello");

    return 0;
}
```

## <a name="requirements"></a>Требования

C++11
