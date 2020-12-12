---
description: 'Дополнительные сведения о: is_integral классе'
title: Класс is_integral
ms.date: 11/04/2016
f1_keywords:
- type_traits/std::is_integral
helpviewer_keywords:
- is_integral class
- is_integral
ms.assetid: fe9279d0-4495-4e88-bf23-153cc6602397
ms.openlocfilehash: db586054614b9a5ef49ffe9fe8b643b35c65a217
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97323705"
---
# <a name="is_integral-class"></a>Класс is_integral

Проверяет, является ли тип целочисленным.

## <a name="syntax"></a>Синтаксис

```cpp
template <class Ty>
struct is_integral;
```

### <a name="parameters"></a>Параметры

*Ty*\
Запрашиваемый тип.

## <a name="remarks"></a>Комментарии

Экземпляр предиката типа содержит значение true, если тип *Ty* является одним из целочисленных типов или `cv-qualified` формой одного из целочисленных типов, в противном случае — значение false.

Целочисленный тип — один из типов **`bool`** , **`char`** ,,, **`unsigned char`** **`signed char`** **`wchar_t`** , **`short`** , **`unsigned short`** , **`int`** , **`unsigned int`** , **`long`** и **`unsigned long`** . Кроме того, с компиляторами, предоставляющими их, целочисленный тип может быть одним из **`long long`** __int64,, **`unsigned long long`** **`__int64`** и **без знака**.

## <a name="example"></a>Пример

```cpp
// std__type_traits__is_integral.cpp
// compile with: /EHsc
#include <type_traits>
#include <iostream>

struct trivial
    {
    int val;
    };

int main()
    {
    std::cout << "is_integral<trivial> == " << std::boolalpha
        << std::is_integral<trivial>::value << std::endl;
    std::cout << "is_integral<int> == " << std::boolalpha
        << std::is_integral<int>::value << std::endl;
    std::cout << "is_integral<float> == " << std::boolalpha
        << std::is_integral<float>::value << std::endl;

    return (0);
    }
```

```Output
is_integral<trivial> == false
is_integral<int> == true
is_integral<float> == false
```

## <a name="requirements"></a>Требования

**Заголовок:**\<type_traits>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[<type_traits>](../standard-library/type-traits.md)\
[Класс is_enum](../standard-library/is-enum-class.md)\
[Класс is_floating_point](../standard-library/is-floating-point-class.md)
