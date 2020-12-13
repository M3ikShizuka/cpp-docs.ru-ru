---
description: 'Дополнительные сведения о: is_rvalue_reference классе'
title: Класс is_rvalue_reference
ms.date: 11/04/2016
f1_keywords:
- type_traits/std::is_rvalue_reference
helpviewer_keywords:
- is_rvalue_reference class
- is_rvalue_reference
ms.assetid: 40a97072-7b5c-4274-9154-298d3dcf064a
ms.openlocfilehash: 1fb3de556f3a8b1b9aa70034a23e5e487336cd56
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97339036"
---
# <a name="is_rvalue_reference-class"></a>Класс is_rvalue_reference

Проверяет, является ли тип ссылкой rvalue.

## <a name="syntax"></a>Синтаксис

```cpp
template <class Ty>
struct is_rvalue_reference;
```

### <a name="parameters"></a>Параметры

*Ty*\
Запрашиваемый тип.

## <a name="remarks"></a>Комментарии

Экземпляр этого предиката типа содержит значение true, если тип *Ty* является [ссылкой rvalue](../cpp/rvalue-reference-declarator-amp-amp.md).

## <a name="requirements"></a>Требования

**Заголовок:**\<type_traits>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[<type_traits>](../standard-library/type-traits.md)\
[Значения lvalue и rvalue](../cpp/lvalues-and-rvalues-visual-cpp.md)
