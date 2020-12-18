---
description: 'Подробнее о следующем: Простое назначение (C)'
title: Простое назначение (C)
ms.date: 11/04/2016
helpviewer_keywords:
- type conversion [C++], simple assignment
- data type conversion [C++], simple assignment
- operators [C], simple assignment
- assignment operators [C++], simple
- simple assignment operator
- equal sign
ms.assetid: e7140a0a-7104-4b3a-b293-7adcc1fdd52b
ms.openlocfilehash: bf8637268c810ed6a75095774ca6ff7b7d3d9e67
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97229903"
---
# <a name="simple-assignment-c"></a>Простое назначение (C)

Оператор простого присваивания присваивает значение правого операнда левому операнду. Значения правого операнда преобразуется в тип выражения присваивания и заменяет значение, хранящееся в объекте, определяемом левым операндом. Применяются правила преобразования для назначений (см. статью [Преобразования назначений](../c-language/assignment-conversions.md)).

```
double x;
int y;

x = y;
```

В этом примере значение переменной `y` преобразуется в тип **`double`** и присваивается переменной `x`.

## <a name="see-also"></a>См. также

[Операторы присваивания C](../c-language/c-assignment-operators.md)
