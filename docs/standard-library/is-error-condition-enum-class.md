---
description: 'Дополнительные сведения о: is_error_condition_enum классе'
title: Класс is_error_condition_enum
ms.date: 11/04/2016
f1_keywords:
- system_error/std::is_error_condition_enum
helpviewer_keywords:
- is_error_condition_enum class
ms.assetid: 752bb87a-c61c-4304-9254-5aaf228b59c0
ms.openlocfilehash: 3fd4f95e06ebee66a1f4d7d0e7de039d26b9f1fe
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97323732"
---
# <a name="is_error_condition_enum-class"></a>Класс is_error_condition_enum

Представляет тип предиката, проверяющий перечисление [error_condition](../standard-library/error-condition-class.md).

## <a name="syntax"></a>Синтаксис

```cpp
template <_Enum>
    class is_error_condition_enum;
```

## <a name="remarks"></a>Remarks

Экземпляр этого [предиката типа](../standard-library/type-traits.md) содержит значение true, если тип `_Enum` является значением перечисления, подходящим для хранения в объекте типа `error_condition`.

Допускается добавление специализации в этот тип для определяемых пользователем типов.

## <a name="see-also"></a>См. также раздел

[<type_traits>](../standard-library/type-traits.md)
