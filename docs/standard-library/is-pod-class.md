---
description: 'Дополнительные сведения о: is_pod классе'
title: Класс is_pod
ms.date: 11/04/2016
f1_keywords:
- type_traits/std::is_pod
helpviewer_keywords:
- is_pod class
- is_pod
ms.assetid: d73ebdee-746b-4082-9fa4-2db71432eb0e
ms.openlocfilehash: b5fd263a0f17831daf7a187c4f0f32a5a635a9d5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97323555"
---
# <a name="is_pod-class"></a>Класс is_pod

Проверяет, является ли тип типом POD.

## <a name="syntax"></a>Синтаксис

```cpp
template <class T>
struct is_pod;
```

### <a name="parameters"></a>Параметры

*T*\
Запрашиваемый тип.

## <a name="remarks"></a>Комментарии

`is_pod<T>::value` имеет значение, **`true`** Если тип *T* является обычным СТАРЫМ данными (Pod). В противном случае — значение **`false`** .

К типам POD относятся арифметические типы, типы перечисления, типы указателей и указатели на типы-члены.

Квалифицированная версия типа POD также обладает типом POD.

Массив данных типа POD также имеет тип POD.

Структура или объединение, все нестатические данные-члены которого имеют типа POD, также обладает типом POD при соблюдении следующих условий:

- Нет объявленных пользователем конструкторов.

- Нет закрытых или защищенных нестатических данных-членов.

- Отсутствие базовых классов.

- Нет виртуальных функций.

- Нет нестатических данных-членов ссылочного типа.

- Нет определяемого пользователем оператора присвоения копирования.

- Нет определяемого пользователем деструктора.

Таким образом, можно рекурсивно создавать структуры POD и массивы, содержащие структуры и массивы POD.

## <a name="example"></a>Пример

```cpp
// std__type_traits__is_pod.cpp
// compile with: /EHsc
#include <type_traits>
#include <iostream>

struct trivial {
    int val;
};

struct throws {
    throws() {}  // User-declared ctor, so not POD

    int val;
};

int main() {
    std::cout << "is_pod<trivial> == " << std::boolalpha
        << std::is_pod<trivial>::value << std::endl;
    std::cout << "is_pod<int> == " << std::boolalpha
        << std::is_pod<int>::value << std::endl;
    std::cout << "is_pod<throws> == " << std::boolalpha
        << std::is_pod<throws>::value << std::endl;

    return (0);
}
```

```Output
is_pod<trivial> == true
is_pod<int> == true
is_pod<throws> == false
```

## <a name="requirements"></a>Требования

**Заголовок:**\<type_traits>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[<type_traits>](../standard-library/type-traits.md)
