---
description: 'Дополнительные сведения о: time_base классе'
title: Класс time_base
ms.date: 11/04/2016
f1_keywords:
- locale/std::time_base
helpviewer_keywords:
- time_base class
ms.assetid: 9ae37f0b-9a42-496e-9870-3d9b71bab8fb
ms.openlocfilehash: cad27546109cf8ed6d8314869a3306f238cc6528
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97289573"
---
# <a name="time_base-class"></a>Класс time_base

Класс выступает в качестве базового класса для аспектов time_get шаблона класса, определяя только перечислимый тип `dateorder` и несколько констант этого типа.

## <a name="syntax"></a>Синтаксис

```cpp
class time_base : public locale::facet {
public:
    enum dateorder {
        no_order,
        dmy,
        mdy,
        ymd,
        ydm
    };
    time_base(size_t _Refs = 0)
    ~time_base();
};
```

## <a name="remarks"></a>Remarks

Каждая константа характеризует свой способ упорядочивания компонентов даты. Используются следующие константы:

- `no_order` Указывает, что порядок не определен.

- `dmy` Указывает день заказа, месяц, год, как в 2 декабря 1979.

- `mdy` Указывает Заказный месяц, день и год, как в 2 декабря 1979 г.

- `ymd` Указывает порядковый номер года, месяца и дня, например 1979/12/2.

- `ydm` Указывает номер года, день и месяц, как в 1979:2 декабря.

## <a name="requirements"></a>Требования

**Заголовок:**\<locale>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[Безопасность потоков в стандартной библиотеке C++](../standard-library/thread-safety-in-the-cpp-standard-library.md)
