---
description: 'Дополнительные сведения о: remove_volatile классе'
title: Класс remove_volatile
ms.date: 11/04/2016
f1_keywords:
- type_traits/std::remove_volatile
helpviewer_keywords:
- remove_volatile class
- remove_volatile
ms.assetid: 8b87e2c2-a581-4eb3-8691-c5603910d61d
ms.openlocfilehash: 45f0ba9ba4685a471f13d0d36ae5080eb667a9f9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97344878"
---
# <a name="remove_volatile-class"></a>Класс remove_volatile

Создает долговременный тип из типа.

## <a name="syntax"></a>Синтаксис

```cpp
template <class T>
struct remove_volatile;

template <class T>
using remove_volatile_t = typename remove_volatile<T>::type;
```

### <a name="parameters"></a>Параметры

*T*\
Тип для изменения.

## <a name="remarks"></a>Комментарии

Экземпляр `remove_volatile<T>` содержит модифицированный тип, который имеет значение, `T1` Если *t* имеет форму `volatile T1` , в противном случае *t*.

## <a name="example"></a>Пример

```cpp
#include <type_traits>
#include <iostream>

int main()
    {
    int *p = (std::remove_volatile_t<volatile int> *)0;

    p = p;  // to quiet "unused" warning
    std::cout << " remove_volatile_t<volatile int> == "
        << typeid(*p).name() << std::endl;

    return (0);
    }
```

```Output
remove_volatile_t<volatile int> == int
```

## <a name="requirements"></a>Требования

**Заголовок:**\<type_traits>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[<type_traits>](../standard-library/type-traits.md)\
[Класс add_volatile](../standard-library/add-volatile-class.md)
