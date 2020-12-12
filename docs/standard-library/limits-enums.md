---
description: 'Дополнительные сведения о: &lt; ограничения &gt; перечислений'
title: Перечисления &lt;limits&gt;
ms.date: 11/04/2016
f1_keywords:
- limits/std::float_denorm_style
- limits/std::float_round_style
ms.assetid: c86680a2-ba97-4ed9-8c20-a448857d7dc5
ms.openlocfilehash: 115122a4901298018df8809be56a7fc69249d700
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97312869"
---
# <a name="ltlimitsgt-enums"></a>Перечисления &lt;limits&gt;

## <a name="float_denorm_style"></a><a name="float_denorm_style"></a> float_denorm_style

Перечисление описывает различные методы, которые могут быть выбраны реализацией для представления ненормализованного значения с плавающей запятой, если оно мало для представления в качестве нормализованного значения:

```cpp
enum float_denorm_style {
    denorm_indeterminate = -1,
    denorm_absent = 0,
    denorm_present = 1    };
```

### <a name="return-value"></a>Возвращаемое значение

Перечисление возвращает:

- `denorm_indeterminate` значение, если не удается определить присутствие или отсутствие денормализованных форм во время преобразования.

- `denorm_absent` Если денормализованные формы отсутствуют.

- `denorm_present` При наличии денормализованных форм.

### <a name="example"></a>Пример

См. раздел [numeric_limits::has_denorm](../standard-library/numeric-limits-class.md#has_denorm) с примером, в котором можно получить доступ к значениям этого перечисления.

## <a name="float_round_style"></a><a name="float_round_style"></a> float_round_style

Перечисление описывает различные методы, которые могут быть выбраны реализацией для округления значения с плавающей запятой до целочисленного.

```cpp
enum float_round_style {
    round_indeterminate = -1,
    round_toward_zero = 0,
    round_to_nearest = 1,
    round_toward_infinity = 2,
    round_toward_neg_infinity = 3    };
```

### <a name="return-value"></a>Возвращаемое значение

Перечисление возвращает:

- `round_indeterminate` значение, если не удается определить метод округления.

- `round_toward_zero` значение, если округление в сторону нуля.

- `round_to_nearest` значение, если округление до ближайшего целого числа.

- `round_toward_infinity` значение, если округление от нуля.

- `round_toward_neg_infinity` значение, если округление до более отрицательного целого числа.

### <a name="example"></a>Пример

См. раздел [numeric_limits::round_style](../standard-library/numeric-limits-class.md#round_style) с примером, в котором можно получить доступ к значениям этого перечисления.
