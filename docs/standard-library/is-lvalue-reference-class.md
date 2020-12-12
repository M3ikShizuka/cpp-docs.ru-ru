---
description: 'Дополнительные сведения о: is_lvalue_reference классе'
title: Класс is_lvalue_reference
ms.date: 11/04/2016
f1_keywords:
- type_traits/std::is_lvalue_reference
helpviewer_keywords:
- is_lvalue_reference class
- is_lvalue_reference
ms.assetid: 7f11896b-935c-4de1-9c87-9d0127f904e2
ms.openlocfilehash: 624849bce456048f4454542db8a03f37771a46d9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97230905"
---
# <a name="is_lvalue_reference-class"></a>Класс is_lvalue_reference

Проверяет, является ли тип ссылкой lvalue.

## <a name="syntax"></a>Синтаксис

```cpp
template <class Ty>
struct is_lvalue_reference;
```

### <a name="parameters"></a>Параметры

*Ty*\
Запрашиваемый тип.

## <a name="remarks"></a>Комментарии

Экземпляр этого предиката типа содержит значение true, если тип *Ty* является ссылкой на объект или функцию, в противном случае — значение false. Обратите внимание, что *Ty* не может быть ссылкой rvalue. Дополнительные сведения о rvalues см. в разделе [Оператор объявления ссылки Rvalue: &&](../cpp/rvalue-reference-declarator-amp-amp.md).

## <a name="requirements"></a>Требования

**Заголовок:**\<type_traits>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[<type_traits>](../standard-library/type-traits.md)\
[Значения lvalue и rvalue](../cpp/lvalues-and-rvalues-visual-cpp.md)
