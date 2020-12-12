---
description: 'Дополнительные сведения о: is_nothrow_constructible классе'
title: Класс is_nothrow_constructible
ms.date: 11/04/2016
f1_keywords:
- type_traits/std::is_nothrow_constructible
helpviewer_keywords:
- is_nothrow_constructible
ms.assetid: 8be3f927-283e-4d67-95a5-8bf5dc4e7a3d
ms.openlocfilehash: 0bb822a42d149a552f18ff4d1b1c723ef9b88172
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97323587"
---
# <a name="is_nothrow_constructible-class"></a>Класс is_nothrow_constructible

Проверяет, является ли тип конструируемым и известным как не выдающим исключения при использовании указанных типов аргументов.

## <a name="syntax"></a>Синтаксис

```cpp
template <class T, class... Args>
struct is_nothrow_constructible;
```

### <a name="parameters"></a>Параметры

*T*\
Запрашиваемый тип.

*Args*\
Типы аргументов для сопоставления в конструкторе *T*.

## <a name="remarks"></a>Комментарии

Экземпляр предиката типа содержит значение true, если тип *T* является конструируемым с помощью типов аргументов в аргументах *args*, и конструктору известно, что компилятор не создает исключение. в противном случае он содержит значение false. Тип *T* — конструируемым, если определение переменной `T t(std::declval<Args>()...);` имеет правильный формат. *T* и все типы в аргументах *args* должны быть полными типами, **`void`** или массивами с неизвестной границей.

## <a name="requirements"></a>Требования

**Заголовок:**\<type_traits>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[<type_traits>](../standard-library/type-traits.md)
