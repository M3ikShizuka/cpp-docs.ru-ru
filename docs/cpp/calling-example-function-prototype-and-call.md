---
description: 'Дополнительные сведения: пример вызова: прототип функции и вызов'
title: Пример вызова. Прототип и вызов функции
ms.date: 11/04/2016
helpviewer_keywords:
- calling conventions, examples [C++]
- examples [C++], calling conventions
ms.assetid: e4275d1f-df2e-4bfc-a162-eb43ec69554a
ms.openlocfilehash: d7d8b68abc030e12d10fc5daa8b56f793d3ea14a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97335592"
---
# <a name="calling-example-function-prototype-and-call"></a>Пример вызова. Прототип и вызов функции

**Блок, относящийся только к системам Microsoft**

В следующем примере показаны результаты вызова функции с использованием различных соглашений о вызовах.

Этот пример основан на следующей схеме функции. Замените `calltype` соответствующим соглашением о вызове.

```cpp
void    calltype MyFunc( char c, short s, int i, double f );
.
.
.
void    MyFunc( char c, short s, int i, double f )
    {
    .
    .
    .
    }
.
.
.
MyFunc ('x', 12, 8192, 2.7183);
```

Дополнительные сведения см. в разделе [результаты вызова примера](../cpp/results-of-calling-example.md).

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Соглашения о вызовах](../cpp/calling-conventions.md)
