---
description: 'Дополнительные сведения о &lt; соотношении: отношение&gt;'
title: '&lt;ratio&gt;'
ms.date: 11/04/2016
f1_keywords:
- <ratio>
- ratio/std::mega
- ratio/std::peta
- ratio/std::ratio_greater
- ratio/std::micro
- ratio/std::ratio_add
- ratio/std::ratio_not_equal
- ratio/std::hecto
- ratio/std::nano
- ratio/std::ratio_less_equal
- ratio/std::ratio_less
- ratio/std::centi
- ratio/std::ratio_greater_equal
- ratio/std::ratio_subtract
- ratio/std::atto
- ratio/std::tera
- ratio/std::milli
- ratio/std::ratio_multiply
- ratio/std::kilo
- ratio/std::ratio_divide
- ratio/std::giga
- ratio/std::pico
- ratio/std::femto
- ratio/std::ratio_equal
- ratio/std::ratio
- ratio/std::exa
- ratio/std::deci
- ratio/std::deca
ms.assetid: 8543e912-2d84-45ea-b3c0-bd7bfacee405
ms.openlocfilehash: a32a8252347de1e6d7bfd5ffd29927c779ce8489
ms.sourcegitcommit: 118e4ad82c0f1c9ac120f105d84224e5fe4cef28
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/12/2021
ms.locfileid: "98126563"
---
# <a name="ltratiogt"></a>&lt;ratio&gt;

Включите стандартный заголовок \<ratio> для определения констант и шаблонов, которые используются для хранения и обработки рациональных чисел во время компиляции.

## <a name="syntax"></a>Синтаксис

```cpp
#include <ratio>
```

### <a name="ratio-template"></a>Шаблон соотношения

```cpp
template<std::intmax_t Numerator, std::intmax_t Denominator = 1>
struct ratio // holds the ratio of Numerator to Denominator
{
   static constexpr std::intmax_t num;
   static constexpr std::intmax_t den;
   typedef ratio<num, den> type;
}
```

Шаблон `ratio` определяет статические константы `num` и `den` такие элементы `num`  /  `den` = = числитель/знаменатель и `num` `den` не имеют общих факторов. `num` / `den` значение, представленное шаблоном класса. Таким образом, `type` обозначает создание экземпляра `ratio<num, den>` .

### <a name="specializations"></a>Специализации

\<ratio> также определяет специализации `ratio` , которые имеют следующую форму.

`template <class R1, class R2> struct ratio_specialization`

Каждая специализация принимает два параметра-шаблона, которые также должны быть специализациями `ratio`. Значение `type` определяется связанной логической операцией.

|Имя|Значение `type`|
|----------|------------------|
|`ratio_add`|`R1 + R2`|
|`ratio_divide`|`R1 / R2`|
|`ratio_equal`|`R1 == R2`|
|`ratio_greater`|`R1 > R2`|
|`ratio_greater_equal`|`R1 >= R2`|
|`ratio_less`|`R1 < R2`|
|`ratio_less_equal`|`R1 <= R2`|
|`ratio_multiply`|`R1 * R2`|
|`ratio_not_equal`|`!(R1 == R2)`|
|`ratio_subtract`|`R1 - R2`|

### <a name="typedefs"></a>определения типов

Для удобства заголовок определяет коэффициенты для стандартных префиксов SI:

```cpp
typedef ratio<1, 1000000000000000000> atto;
typedef ratio<1, 1000000000000000> femto;
typedef ratio<1, 1000000000000> pico;
typedef ratio<1, 1000000000> nano;
typedef ratio<1, 1000000> micro;
typedef ratio<1, 1000> milli;
typedef ratio<1, 100> centi;
typedef ratio<1, 10> deci;
typedef ratio<10, 1> deca;
typedef ratio<100, 1> hecto;
typedef ratio<1000, 1> kilo;
typedef ratio<1000000, 1> mega;
typedef ratio<1000000000, 1> giga;
typedef ratio<1000000000000, 1> tera;
typedef ratio<1000000000000000, 1> peta;
typedef ratio<1000000000000000000, 1> exa;
```

## <a name="see-also"></a>См. также раздел

[Справочник по файлам заголовков](../standard-library/cpp-standard-library-header-files.md)
