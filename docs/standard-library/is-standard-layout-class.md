---
description: 'Дополнительные сведения о: is_standard_layout классе'
title: Класс is_standard_layout
ms.date: 11/04/2016
f1_keywords:
- type_traits/std::is_standard_layout
helpviewer_keywords:
- is_standard_layout class
- is_standard_layout
ms.assetid: 15ccf111-f537-45ef-b552-59152a7ba312
ms.openlocfilehash: 8f1f24fcb29e862dff10c2a51d1c9d0b2b28541f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97271256"
---
# <a name="is_standard_layout-class"></a>Класс is_standard_layout

Проверяет, является ли тип стандартным макетом.

## <a name="syntax"></a>Синтаксис

```cpp
template <class Ty>
struct is_standard_layout;
```

### <a name="parameters"></a>Параметры

*Ty*\
Запрашиваемый тип.

## <a name="remarks"></a>Комментарии

Экземпляр этого предиката типа содержит значение true, если тип *Ty* является классом, имеющим стандартный макет объектов-членов в памяти, в противном случае — значение false.

## <a name="requirements"></a>Требования

**Заголовок:**\<type_traits>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[<type_traits>](../standard-library/type-traits.md)
