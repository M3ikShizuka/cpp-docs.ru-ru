---
description: 'Дополнительные сведения о: is_copy_assignable классе'
title: Класс is_copy_assignable
ms.date: 11/04/2016
f1_keywords:
- type_traits/std::is_copy_assignable
helpviewer_keywords:
- is_copy_assignable
ms.assetid: 3ae6bca1-85fb-4829-9ee9-0183b081ff50
ms.openlocfilehash: f13752ce74f316f180fb874572efaf15d1c06c31
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97323802"
---
# <a name="is_copy_assignable-class"></a>Класс is_copy_assignable

Проверяет, может ли тип быть скопирован при присвоении значения.

## <a name="syntax"></a>Синтаксис

```cpp
template <class Ty>
struct is_copy_assignable;
```

### <a name="parameters"></a>Параметры

*Ty*\
Запрашиваемый тип.

## <a name="remarks"></a>Комментарии

Экземпляр предиката типа содержит значение true, если тип *Ty* является классом с оператором присваивания копии, в противном случае — значение false. Эквивалентно is_assignable \<Ty&, const Ty&> .

## <a name="requirements"></a>Требования

**Заголовок:**\<type_traits>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[<type_traits>](../standard-library/type-traits.md)
