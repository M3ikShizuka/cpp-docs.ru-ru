---
description: 'Дополнительные сведения о: is_trivially_constructible классе'
title: Класс is_trivially_constructible
ms.date: 11/04/2016
f1_keywords:
- type_traits/std::is_trivially_constructible
helpviewer_keywords:
- is_trivially_constructible
ms.assetid: 3fa918c1-e66f-4d0e-a11b-be1fb2c02e7b
ms.openlocfilehash: 4a5c3e20366c4e87aa731c6d6a69787286b947b9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97247635"
---
# <a name="is_trivially_constructible-class"></a>Класс is_trivially_constructible

Проверяет, является ли тип просто создаваемым при использовании указанных типов аргументов.

## <a name="syntax"></a>Синтаксис

```cpp
template <class T, class... Args>
struct is_trivially_constructible;
```

### <a name="parameters"></a>Параметры

*T*\
Запрашиваемый тип.

*Args*\
Типы аргументов для сопоставления в конструкторе *T*.

## <a name="remarks"></a>Комментарии

Экземпляр предиката типа содержит значение true, если тип *T* является тривиально конструируемым с помощью типов аргументов в аргументах *args*, в противном случае — значение false. Тип *T* является тривиальным конструируемым, если определение переменной `T t(std::declval<Args>()...);` имеет правильный формат и известно, что он вызывает не нетривиальные операции. *T* и все типы в аргументах *args* должны быть полными типами, **`void`** или массивами с неизвестной границей.

## <a name="requirements"></a>Требования

**Заголовок:**\<type_traits>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[<type_traits>](../standard-library/type-traits.md)
