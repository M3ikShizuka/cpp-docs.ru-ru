---
description: 'Дополнительные сведения: &lt; случайные &gt; функции'
title: Функции &lt;random&gt;
ms.date: 09/04/2019
f1_keywords:
- random/std::generate_canonical
ms.assetid: 2ac9ec59-619b-4b85-a425-f729277c1bc8
helpviewer_keywords:
- std::generate_canonical
ms.openlocfilehash: 39670fcd9b200a6bd56656bbfa07391fdd0d96be
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97163344"
---
# <a name="ltrandomgt-functions"></a>Функции &lt;random&gt;

## <a name="generate_canonical"></a><a name="generate_canonical"></a> generate_canonical

Возвращает значение с плавающей запятой из случайной последовательности.

```cpp
template <class RealType, size_t Bits, class Generator>
RealType generate_canonical(Generator& Gen);
```

### <a name="parameters"></a>Параметры

*реалтипе*\
Тип с плавающей запятой. Возможные типы см. в разделе [\<random>](../standard-library/random.md) .

*Числа*\
Количество используемых битов случайности.

*Формирования*\
Класс генератора случайных чисел.

*Операций*\
Ссылка на экземпляр генератора случайных чисел типа " *генератор*".

### <a name="remarks"></a>Комментарии

Функция шаблона вызывает `operator()` многократное  обращение и упаковывает возвращаемые значения в значение с плавающей запятой `x` типа *реалтипе* до тех пор, пока не собрало указанное число битов мантиссаа в `x` . Указанное число является меньшим из *битов* (значение которого должно быть ненулевым) и полным числом битов мантисса в *реалтипе*. Первый вызов предоставляет младшие разряды. Функция возвращает `x`.
