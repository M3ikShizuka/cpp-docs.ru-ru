---
description: 'Дополнительные сведения о операторе: преобразования (# @)'
title: Оператор преобразования в символы (#@)
ms.date: 08/29/2019
f1_keywords:
- '#@'
helpviewer_keywords:
- preprocessor, operators
- charizing operator
- '#@ preprocessor operator'
ms.assetid: dee03314-d27c-4063-965c-64756efbef22
ms.openlocfilehash: 6d04aa24c75153957bd6fd09824f4e94e36fd38f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97300870"
---
# <a name="charizing-operator-"></a>Оператор преобразования в символы (#@)

**Блок, относящийся только к системам Microsoft**

Оператор образования символа может использоваться только в аргументах макросов. Если `#@` перед формальным параметром в определении макроса, фактический аргумент заключается в одинарные кавычки и обрабатывается как символ при расширении макроса. Пример:

```cpp
#define makechar(x)  #@x
```

приводит к разворачиванию оператора

```cpp
a = makechar(b);
```

в выражение

```cpp
a = 'b';
```

Символ одинарной кавычки ( `'` ) нельзя использовать с оператором преобразования.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Операторы препроцессора](../preprocessor/preprocessor-operators.md)
