---
description: 'Дополнительные сведения о: underlying_type классе'
title: Класс underlying_type
ms.date: 11/04/2016
f1_keywords:
- type_traits/std::underlying_type
helpviewer_keywords:
- underlying_type
ms.assetid: 691ddce3-2677-4480-bd35-d933fab85d3e
ms.openlocfilehash: e717abe854f13fc96926deba1d4bf177529618cf
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97132708"
---
# <a name="underlying_type-class"></a>Класс underlying_type

Создает базовый целочисленный тип для типа перечисления.

## <a name="syntax"></a>Синтаксис

```cpp
template <class T>
struct underlying_type;
```

### <a name="parameters"></a>Параметры

*T*\
Тип для изменения.

## <a name="remarks"></a>Комментарии

`type`Typedef элемента шаблона класса называет базовый целочисленный тип *t*, если *T* является типом перечисления, в противном случае typedef не существует `type` .

## <a name="requirements"></a>Требования

**Заголовок:**\<type_traits>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[<type_traits>](../standard-library/type-traits.md)
