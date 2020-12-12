---
description: 'Дополнительные сведения о: is_nothrow_move_constructible классе'
title: Класс is_nothrow_move_constructible
ms.date: 11/04/2016
f1_keywords:
- type_traits/std::is_nothrow_move_constructible
helpviewer_keywords:
- is_nothrow_move_constructible
ms.assetid: d186d97b-7b89-470a-8d30-993046a83379
ms.openlocfilehash: 9ab9d1dfdba532bfda3111831f389a94a49af936
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97323601"
---
# <a name="is_nothrow_move_constructible-class"></a>Класс is_nothrow_move_constructible

Проверяет, имеет ли тип **`nothrow`** конструктор перемещения.

## <a name="syntax"></a>Синтаксис

```cpp
template <class Ty>
struct is_nothrow_move_constructible;
```

### <a name="parameters"></a>Параметры

*Ty*\
Запрашиваемый тип.

## <a name="remarks"></a>Комментарии

Экземпляр предиката типа содержит значение true, если тип *Ty* имеет конструктор перемещения "Throw", в противном случае — значение false.

## <a name="requirements"></a>Требования

**Заголовок:**\<type_traits>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[<type_traits>](../standard-library/type-traits.md)
