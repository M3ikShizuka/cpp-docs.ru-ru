---
description: 'Дополнительные сведения о: is_error_code_enum классе'
title: Класс is_error_code_enum
ms.date: 11/04/2016
f1_keywords:
- system_error/std::is_error_code_enum
helpviewer_keywords:
- is_error_code_enum class
ms.assetid: cee5be2d-7c20-4cec-a352-1ab8b7d32601
ms.openlocfilehash: 359f15c3d809435df81408a721a0c9ad11c1e7e5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97323759"
---
# <a name="is_error_code_enum-class"></a>Класс is_error_code_enum

Представляет тип предиката, проверяющий перечисление [error_code](../standard-library/error-code-class.md).

## <a name="syntax"></a>Синтаксис

```cpp
template <_Enum>
    class is_error_code_enum;
```

## <a name="remarks"></a>Remarks

Экземпляр этого [предиката типа](../standard-library/type-traits.md) содержит значение true, если тип `_Enum` является значением перечисления, подходящим для хранения в объекте типа `error_code`.

Допускается добавление специализации в этот тип для определяемых пользователем типов.

## <a name="see-also"></a>См. также раздел

[<type_traits>](../standard-library/type-traits.md)
