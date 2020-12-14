---
description: 'Дополнительные сведения о: money_base классе'
title: Класс money_base
ms.date: 11/04/2016
f1_keywords:
- xlocmon/std::money_base
helpviewer_keywords:
- money_base class
ms.assetid: 1a303c15-9272-4f26-ae16-dcf43a0fd38a
ms.openlocfilehash: 295984cfed4d6fdd47c772e29765c1484f52d32a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97230475"
---
# <a name="money_base-class"></a>Класс money_base

Класс описывает перечисление и структуру, общую для всех специализаций шаблона класса [moneypunct](../standard-library/moneypunct-class.md).

## <a name="syntax"></a>Синтаксис

```cpp
struct pattern
{
   char field[_PATTERN_FIELD_SIZE];
};
```

## <a name="remarks"></a>Remarks

Перечисление `part` описывает возможные значения в элементах поля массива в шаблоне структуры. Значения `part` :

- `none` значение, чтобы сопоставить ноль или больше пробелов или ничего не создавать.

- `sign` для сопоставления или создания положительного или отрицательного знака.

- `space` значение, чтобы сопоставить ноль или больше пробелов или сгенерировать пробел.

- `symbol` для сопоставления или создания символа валюты.

- `value` для сопоставления или создания денежного значения.

## <a name="requirements"></a>Требования

**Заголовок:**\<locale>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[Безопасность потоков в стандартной библиотеке C++](../standard-library/thread-safety-in-the-cpp-standard-library.md)
