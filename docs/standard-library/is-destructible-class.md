---
description: 'Дополнительные сведения о: is_destructible классе'
title: Класс is_destructible
ms.date: 11/04/2016
f1_keywords:
- type_traits/std::is_destructible
helpviewer_keywords:
- is_destructible
ms.assetid: 3bb9b718-1ad5-49ae-93cc-92b93b546b4d
ms.openlocfilehash: fcd41c292c0054553b165529a85e7b23312d3c2e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97231164"
---
# <a name="is_destructible-class"></a>Класс is_destructible

Проверяет, можно ли уничтожить тип.

## <a name="syntax"></a>Синтаксис

```cpp
template <class T>
struct is_destructible;
```

### <a name="parameters"></a>Параметры

*T*\
Запрашиваемый тип.

## <a name="remarks"></a>Комментарии

Экземпляр предиката типа содержит значение true, если тип *T* является типом можно уничтожить, в противном случае — значение false. К типам, которые можно уничтожить, относятся ссылочные типы, типы объектов и типы, для которых при типе `U` , равном `remove_all_extents_t<T>` , невычисленный операнд `std::declval<U&>.~U()` имеет правильный формат. Другие типы, включая неполные типы, **`void`** и типы функций, не являются типами можно уничтожить.

## <a name="requirements"></a>Требования

**Заголовок:**\<type_traits>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[<type_traits>](../standard-library/type-traits.md)
