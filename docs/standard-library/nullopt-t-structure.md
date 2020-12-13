---
description: 'Дополнительные сведения о: nullopt_t struct'
title: Структура nullopt_t
ms.date: 08/04/2019
f1_keywords:
- optional/std::nullopt_t
- optional/std::nullopt
ms.openlocfilehash: 7a597dcc5f15843f125dc7572dc4c5694320f0bb
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97338115"
---
# <a name="nullopt_t-struct"></a>Структура nullopt_t

`nullopt_t`Тип — уникальный, пустой тип, который указывает, что [необязательный](optional-class.md) объект не содержит значения.

Константа `nullopt` типа `nullopt_t` указывает, что `optional` тип имеет неинициализированное состояние. Его можно использовать для инициализации `optional` объекта или по сравнению с одним.

## <a name="syntax"></a>Синтаксис

```cpp
struct nullopt_t;
inline constexpr nullopt_t nullopt{ /*implementation-defined*/ };
```

## <a name="see-also"></a>См. также раздел

[\<optional>](optional.md)\
[необязательный класс](optional-class.md)
