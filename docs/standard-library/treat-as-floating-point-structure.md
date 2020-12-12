---
description: 'Дополнительные сведения: структура treat_as_floating_point'
title: Структура treat_as_floating_point
ms.date: 11/04/2016
f1_keywords:
- chrono/std::chrono::treat_as_floating_point
ms.assetid: d0a2161c-bbb2-4924-8961-7568d5ad5434
ms.openlocfilehash: 498421d454de1e15ea52282665bcf9ae7d045946
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97169064"
---
# <a name="treat_as_floating_point-structure"></a>Структура treat_as_floating_point

Указывает, может ли тип `Rep` рассматриваться как тип с плавающей запятой.

## <a name="syntax"></a>Синтаксис

```cpp
template <class Rep>
struct treat_as_floating_point : is_floating_point<Rep>;
```

## <a name="remarks"></a>Remarks

`Rep` можно рассматривать как тип с плавающей запятой, только если специализация `treat_as_floating_point<Rep>` является производной от [true_type](../standard-library/type-traits-typedefs.md#true_type). Шаблон класса может быть специализированным для определяемого пользователем типа.

## <a name="requirements"></a>Требования

**Заголовок:**\<chrono>

**Пространство имен:** std::chrono

## <a name="see-also"></a>См. также раздел

[Справочник по файлам заголовков](../standard-library/cpp-standard-library-header-files.md)\
[\<chrono>](../standard-library/chrono.md)
