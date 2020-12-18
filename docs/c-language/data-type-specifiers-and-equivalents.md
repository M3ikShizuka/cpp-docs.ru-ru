---
title: Описатели и эквиваленты типов данных
description: Сведения об описателях типов данных Microsoft Visual C и их эквивалентах.
ms.date: 11/04/2016
helpviewer_keywords:
- type specifiers [C++], list
- widening integers
- data types [C++], equivalents
- sign-extending integral types
- zero-extending
- identifiers, data type
- data types [C++], specifiers
- simple types, names
- type names [C++], simple
ms.openlocfilehash: 6a1231bc19617dddf1cc01d4c5e7db2863f1055f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97207050"
---
# <a name="data-type-specifiers-and-equivalents"></a>Описатели и эквиваленты типов данных

В рамках этой документации в большинстве случаев вместо полных форм описателей типов используются формы, приведенные в следующей таблице. При этом также предполагается, что тип **`char`** является знаковым по умолчанию. В этой документации тип **`char`** эквивалентен типу **`signed char`** .

## <a name="type-specifiers-and-equivalents"></a>Описатели типов и их эквиваленты

| Спецификаторы типов | Эквиваленты |
|--|--|
| **`signed char`** <sup>1</sup> | **`char`** |
| **`signed int`** | **`signed`** , **`int`** |
| **`signed short int`** | **`short`**, **`signed short`** |
| **`signed long int`** | **`long`**, **`signed long`** |
| **`unsigned char`** | — |
| **`unsigned int`** | **`unsigned`** |
| **`unsigned short int`** | **`unsigned short`** |
| **`unsigned long int`** | **`unsigned long`** |
| **`float`** | — |
| **`long double`** <sup>2</sup> | — |

<sup>1</sup> Если вы указали, что тип **`char`** по умолчанию является беззнаковым (указав параметр компилятора **`/J`** ), вы не сможете сократить **`signed char`** до **`char`** .

<sup>2</sup> В 32- и 64-разрядных операционных системах компилятор Microsoft С устанавливает соответствие между типами **`long double`** и **`double`** .

**Только для систем Майкрософт**

При помощи параметра компилятора **`/J`** можно указать, что тип **`char`** по умолчанию является не **`signed char`** , а **`unsigned char`** . При использовании этого параметра описатель **`char`** означает то же, что и **`unsigned char`** . Для объявления знакового символьного значения необходимо использовать ключевое слово **`signed`** . Если значение **`char`** явным образом объявлено как **`signed`** , то параметр **`/J`** на него не влияет и его расширение до типа **`int`** выполняется с расширением знака. Расширение типа **`char`** до типа **`int`** выполняется с дополнением нулями.

**ОКОНЧАНИЕ Только для систем Майкрософт**

## <a name="see-also"></a>См. также

[Спецификаторы типов C](../c-language/c-type-specifiers.md)
