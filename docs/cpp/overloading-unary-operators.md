---
description: 'Дополнительные сведения: перегрузка унарных операторов'
title: Перегрузка унарных операторов
ms.date: 11/04/2016
helpviewer_keywords:
- unary operators [C++], plus
- increment operators [C++], overloaded
- unary operators [C++], minus
- operators [C++], unary
- redefinable unary operators [C++]
- unary operators [C++]
- pointer dereference operator overloading
- plus operator
ms.assetid: 7683ef08-42a4-4283-928f-d3dd4f3ab4c0
ms.openlocfilehash: 2e0a2d2b902403ee5ed34a95b6d282d7c2199795
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97146059"
---
# <a name="overloading-unary-operators"></a>Перегрузка унарных операторов

Перегрузке могут быть подвергнуты следующие унарные операторы.

1. `!` ([логическое не](../cpp/logical-negation-operator-exclpt.md))

1. `&` ([адрес](../cpp/address-of-operator-amp.md))

1. `~` ([дополнение одного](../cpp/one-s-complement-operator-tilde.md))

1. `*` ([разыменование указателя](../cpp/indirection-operator-star.md))

1. `+` ([унарный плюс](../cpp/additive-operators-plus-and.md))

1. `-` ([унарное отрицание](../cpp/additive-operators-plus-and.md))

1. `++` ([приращение](../cpp/prefix-increment-and-decrement-operators-increment-and-decrement.md))

1. `--` ([декремента](../cpp/prefix-increment-and-decrement-operators-increment-and-decrement.md))

1. операторы преобразования

Постфиксные операторы инкремента и декремента ( `++` и `--` ) обрабатываются отдельно при [инкременте и декремента](../cpp/increment-and-decrement-operator-overloading-cpp.md).

Операторы преобразования также обсуждаются в отдельном разделе. см. раздел [преобразование определяемого пользователем типа](../cpp/user-defined-type-conversions-cpp.md).

Следующие правила распространяются на все остальные унарные операторы. Чтобы объявить функцию унарного оператора как нестатический член, необходимо объявить ее в форме

> *RET-тип* **`operator`** *Op* **()**

где *RET-Type* — это тип возвращаемого значения, а *Op* — один из операторов, перечисленных в предыдущей таблице.

Чтобы объявить функцию унарного оператора как глобальную функцию, необходимо объявить ее в форме

> *RET-тип* **`operator`** *Op* **(** *arg* **)**

где *RET-Type* и *Op* описаны для функций *оператора-члена, а аргумент является* аргументом типа класса, с которым будет работать.

> [!NOTE]
> Не существует ограничения на типы возвращаемого значения унарных операторов. Например, логическому НЕ (`!`) имеет смысл возвращать целочисленное значение, однако это не реализовано принудительно.

## <a name="see-also"></a>См. также раздел

[Перегрузка операторов](../cpp/operator-overloading.md)
