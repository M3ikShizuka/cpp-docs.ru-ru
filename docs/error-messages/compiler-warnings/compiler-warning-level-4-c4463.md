---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 4) C4463'
title: Предупреждение компилятора (уровень 4) C4463
ms.date: 11/04/2016
f1_keywords:
- C4463
helpviewer_keywords:
- C4463
ms.assetid: a07ae70c-db4e-472b-8b58-9137d9997323
ms.openlocfilehash: fe4ea13c50e16bf5b72f5753fa989970db3cadde
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97251327"
---
# <a name="compiler-warning-level-4-c4463"></a>Предупреждение компилятора (уровень 4) C4463

> полн Присвоение *значения* битовому полю, которое может содержать только значения от *low_value* до *high_value*

Назначенное *значение* выходит за пределы диапазона значений, которые могут храниться в битовом поле. Типы битовых полей со знаком используют бит высокого порядка для знака, поэтому, если *n* — это размер битового поля, диапазон для битовых полей со знаком имеет значение-2 <sup>n – 1</sup> <sup>– 2,</sup>а в качестве битовых полей без знака — от 0 до 2 <sup>n</sup>-1.

## <a name="example"></a>Пример

В этом примере создается C4463, поскольку он пытается присвоить значение 3 к битовому полю типа **`int`** с размером 2, который имеет диапазон от-2 до 1.

Чтобы устранить эту проблему, можно изменить присвоенное значение на что-то в допустимом диапазоне. Если битовое поле предназначено для хранения беззнаковых значений в диапазоне от 0 до 3, можно изменить тип объявления на **`unsigned`** . Если поле предназначено для хранения значений в диапазоне от-4 до 3, можно изменить размер битового поля на 3.

```cpp
// C4463_overflow.cpp
// compile with: cl /W4 /EHsc C4463_overflow.cpp
struct S {
    int x : 2; // int type treats high-order bit as sign
};

int main() {
    S s;
    s.x = 3; // warning C4463: overflow; assigning 3
    // to bit-field that can only hold values from -2 to 1
    // To fix, change assigned value to fit in range,
    // increase size of bitfield, and/or change base type
    // to unsigned.
}
```
