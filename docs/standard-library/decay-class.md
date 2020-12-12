---
description: 'Дополнительные сведения о: Decay Class'
title: Класс decay
ms.date: 11/04/2016
f1_keywords:
- type_traits/std::decay
helpviewer_keywords:
- decay class
ms.assetid: 96baa2fd-c8e0-49af-be91-ba375ba7f9dc
ms.openlocfilehash: 6f6a1ebd31af44a48eaf400f9dccefdbd8ca3d01
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97324605"
---
# <a name="decay-class"></a>Класс decay

Создает тип в качестве передаваемого значения. Создает тип, не являющийся ссылочным, константным, временным, или создает указатель на тип из функции или типа массива.

## <a name="syntax"></a>Синтаксис

```cpp
template <class T>
struct decay;

template <class T>
using decay_t = typename decay<T>::type;
```

### <a name="parameters"></a>Параметры

*T*\
Тип для изменения.

## <a name="remarks"></a>Комментарии

Используйте шаблон decay для создания результирующего типа, как если бы тип был передан по значению в качестве аргумента. Typedef члена шаблона класса `type` содержит измененный тип, который определен на следующих этапах:

- Тип `U` определяется как `remove_reference<T>::type`.

- Если `is_array<U>::value` имеет значение true, измененный тип `type` имеет значение `remove_extent<U>::type *`.

- Если же `is_function<U>::value` имеет значение true, измененный тип `type` имеет значение `add_pointer<U>::type`.

- В противном случае измененный тип `type` имеет значение `remove_cv<U>::type`.

## <a name="requirements"></a>Требования

**Заголовок:**\<type_traits>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[<type_traits>](../standard-library/type-traits.md)
