---
description: 'Дополнительные сведения: выражения с унарными операторами'
title: Выражения с унарными операторами
ms.date: 11/04/2016
helpviewer_keywords:
- expressions [C++], unary operators
- unary operators [C++], expressions with
- expressions [C++], operators
ms.assetid: 1217685b-b85d-4b48-9ff4-d90f56a26c1b
ms.openlocfilehash: 6714727d0a4b2c386c37550151df21062534376e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97186510"
---
# <a name="expressions-with-unary-operators"></a>Выражения с унарными операторами

Унарные операторы действуют только на один операнд в выражении. Ниже приводится список унарных операторов:

- [Оператор косвенного обращения (*)](../cpp/indirection-operator-star.md)

- [Оператор взятия адреса (&)](../cpp/address-of-operator-amp.md)

- [Оператор унарного плюса (+)](../cpp/unary-plus-and-negation-operators-plus-and.md)

- [Унарный оператор отрицания (-)](../cpp/unary-plus-and-negation-operators-plus-and.md)

- [Оператор логического отрицания (!)](../cpp/logical-negation-operator-exclpt.md)

- [Оператор дополнения до единицы (~)](../cpp/one-s-complement-operator-tilde.md)

- [Префиксный оператор инкремента (++)](../cpp/prefix-increment-and-decrement-operators-increment-and-decrement.md)

- [Оператор префикса декремента (--)](../cpp/prefix-increment-and-decrement-operators-increment-and-decrement.md)

- [Оператор CAST ()](../cpp/cast-operator-parens.md)

- [`sizeof` станции](../cpp/sizeof-operator.md)

- [`__uuidof` станции](../cpp/uuidof-operator.md)

- [`alignof` станции](../cpp/alignof-operator.md)

- [`new` станции](../cpp/new-operator-cpp.md)

- [`delete` станции](../cpp/delete-operator-cpp.md)

Эти операторы имеют ассоциативность справа налево. Обычно синтаксис унарных выражений предшествует синтаксису постфиксных или основных выражений.

Ниже перечислены возможные формы унарных выражений.

- *postfix-expression*

- `++` *unary-expression*

- `--` *unary-expression*

- приведение *унарных операторов* *-выражение*

- **`sizeof`***унарное выражение*

- `sizeof(`*имя типа*`)`

- `decltype(`*выражение*`)`

- *выражение выделения*

- *unallocation — выражение*

Любое *постфиксное* выражение считается *унарным выражением*, а так как любое первичное выражение считается *постфиксным выражением*, любые первичные выражения считаются также *унарным выражением* . Дополнительные сведения см. в разделе [постфиксные выражения](../cpp/postfix-expressions.md) и [Первичные выражения](../cpp/primary-expressions.md).

*Унарный оператор* состоит из одного или нескольких следующих символов:`* & + - ! ~`

*Выражение CAST-Expression* является унарным выражением с необязательным приведением для изменения типа. Дополнительные сведения см. в разделе [оператор CAST: ()](../cpp/cast-operator-parens.md).

*Выражение* может быть любым выражением. Дополнительные сведения см. в разделе [выражения](../cpp/expressions-cpp.md).

*Выражение выделения* ссылается на **`new`** оператор. *Выражение освобождения —* это **`delete`** оператор. Дополнительные сведения см. по ссылкам, приведенным выше.

## <a name="see-also"></a>См. также раздел

[Типы выражений](../cpp/types-of-expressions.md)
