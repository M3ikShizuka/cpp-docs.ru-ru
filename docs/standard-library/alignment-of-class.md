---
description: 'Дополнительные сведения о: alignment_of классе'
title: Класс alignment_of
ms.date: 12/11/2019
f1_keywords:
- type_traits/std::alignment_of
helpviewer_keywords:
- alignment_of class
- alignment_of
ms.assetid: 4141c59a-f94e-41c4-93fd-9ea578b27387
ms.openlocfilehash: 7e1eeafb259b71f24cb272c079cdb485bb8e1b4a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97163656"
---
# <a name="alignment_of-class"></a>Класс alignment_of

Получает выравнивание указанного типа. Эта структура реализуется с точки зрения [`alignof`](../cpp/alignment-cpp-declarations.md) . Используйте **`alignof`** напрямую, если нужно просто запросить значение выравнивания. Используется `alignment_of` , если требуется целая константа, например при отправке тегов.

## <a name="syntax"></a>Синтаксис

```cpp
template <class Ty>
struct alignment_of;
```

### <a name="parameters"></a>Параметры

*Ty*\
Запрашиваемый тип.

## <a name="remarks"></a>Комментарии

Запрос типа содержит значение выравнивания типа *Ty*.

## <a name="requirements"></a>Требования

**Заголовок:**\<type_traits>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[`<type_traits>`](type-traits.md)\
[`aligned_storage` См](aligned-storage-class.md)
