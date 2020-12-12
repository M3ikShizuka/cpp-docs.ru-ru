---
description: 'Дополнительные сведения о: is_floating_point классе'
title: Класс is_floating_point
ms.date: 11/04/2016
f1_keywords:
- type_traits/std::is_floating_point
helpviewer_keywords:
- is_floating_point class
- is_floating_point
ms.assetid: 070679c1-115b-4ee4-8ab7-f52e5d9e157f
ms.openlocfilehash: e1ace01a88c103646e9daa6ece82b9c3c3c2978a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97230982"
---
# <a name="is_floating_point-class"></a>Класс is_floating_point

Проверяет, является ли тип типом с плавающей запятой.

## <a name="syntax"></a>Синтаксис

```cpp
template <class Ty>
struct is_floating_point;
```

### <a name="parameters"></a>Параметры

*Ty*\
Запрашиваемый тип.

## <a name="remarks"></a>Комментарии

Экземпляр предиката типа содержит значение true, если тип *Ty* является типом с плавающей запятой или `cv-qualified` формой типа с плавающей запятой, в противном случае — значение false.

Тип с плавающей запятой — один из типов **`float`** , **`double`** или **`long double`** .

## <a name="example"></a>Пример

```cpp
// std__type_traits__is_floating_point.cpp
// compile with: /EHsc
#include <type_traits>
#include <iostream>

struct trivial
    {
    int val;
    };

int main()
    {
    std::cout << "is_floating_point<trivial> == " << std::boolalpha
        << std::is_floating_point<trivial>::value << std::endl;
    std::cout << "is_floating_point<int> == " << std::boolalpha
        << std::is_floating_point<int>::value << std::endl;
    std::cout << "is_floating_point<float> == " << std::boolalpha
        << std::is_floating_point<float>::value << std::endl;

    return (0);
    }
```

```Output
is_floating_point<trivial> == false
is_floating_point<int> == false
is_floating_point<float> == true
```

## <a name="requirements"></a>Требования

**Заголовок:**\<type_traits>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[<type_traits>](../standard-library/type-traits.md)\
[Класс is_integral](../standard-library/is-integral-class.md)
