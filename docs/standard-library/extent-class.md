---
description: 'Дополнительные сведения о: классе экстента'
title: Класс extent
ms.date: 11/04/2016
f1_keywords:
- type_traits/std::extent
helpviewer_keywords:
- extent class
- extent
ms.assetid: 6d16263d-90b2-4330-9ec7-b59ed898792d
ms.openlocfilehash: d3db49db99d2cb7a241ca3b69c48fa6bcf2cb490
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97324390"
---
# <a name="extent-class"></a>Класс extent

Получает измерение массива.

## <a name="syntax"></a>Синтаксис

```cpp
template <class Ty, unsigned I = 0>
struct extent;
```

### <a name="parameters"></a>Параметры

*Ty*\
Запрашиваемый тип.

*Сохранении*\
Массив, привязанный к запросу.

## <a name="remarks"></a>Комментарии

Если *Ty* является типом массива, имеющего по крайней мере *i* единицу измерения, то запрос типа содержит количество элементов в измерении, заданном параметром *i*. Если *Ty* не является типом массива или его ранг меньше *I*, или если *i* равен нулю и *Ty* имеет тип "массив с неизвестной границей `U` ", запрос типа содержит значение 0.

## <a name="example"></a>Пример

```cpp
// std__type_traits__extent.cpp
// compile with: /EHsc
#include <type_traits>
#include <iostream>

int main()
    {
    std::cout << "extent 0 == "
        << std::extent<int[5][10]>::value << std::endl;
    std::cout << "extent 1 == "
        << std::extent<int[5][10], 1>::value << std::endl;

    return (0);
    }
```

```Output
extent 0 == 5
extent 1 == 10
```

## <a name="requirements"></a>Требования

**Заголовок:**\<type_traits>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[<type_traits>](../standard-library/type-traits.md)\
[Класс remove_all_extents](../standard-library/remove-all-extents-class.md)\
[Класс remove_extent](../standard-library/remove-extent-class.md)
