---
description: 'Дополнительные сведения о: is_null_pointer классе'
title: Класс is_null_pointer
ms.date: 11/04/2016
f1_keywords:
- type_traits/std::is_null_pointer
helpviewer_keywords:
- is_null_pointer
ms.assetid: f3b3601b-f162-4803-a6e9-dabf5c3876cc
ms.openlocfilehash: 91a8b6a27668af72d7641ce1fe36dafc119f5aa7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97230670"
---
# <a name="is_null_pointer-class"></a>Класс is_null_pointer

Проверяет, является ли тип std::nullptr_t.

## <a name="syntax"></a>Синтаксис

```cpp
template <class T>
struct is_null_pointer;
```

### <a name="parameters"></a>Параметры

*T*\
Запрашиваемый тип.

## <a name="remarks"></a>Комментарии

Экземпляр предиката типа содержит значение true, если тип *T* — `std::nullptr_t` , в противном случае — значение false.

## <a name="requirements"></a>Требования

**Заголовок:**\<type_traits>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[<type_traits>](../standard-library/type-traits.md)
