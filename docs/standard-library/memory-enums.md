---
description: Дополнительные сведения о &lt; &gt; перечислителях памяти
title: Перечисления &lt;memory&gt;
ms.date: 11/04/2016
f1_keywords:
- memory/std::pointer_safety
ms.assetid: b9be0a7b-0beb-40b2-8183-911de371c6b9
ms.openlocfilehash: da9bb22a6095f74b94e1745210fa55061ecf3c71
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97149101"
---
# <a name="ltmemorygt-enums"></a>Перечисления &lt;memory&gt;

## <a name="pointer_safety-enumeration"></a><a name="pointer_safety"></a> Перечисление pointer_safety

Перечисление возможных значений, возвращаемых `get_pointer_safety`.

```cpp
class pointer_safety {
   relaxed,
   preferred,
   strict
};
```

### <a name="remarks"></a>Комментарии

Область **`enum`** определяет значения, которые могут быть возвращены `get_pointer_safety()` :

`relaxed` — указатели, наследованные небезопасно (указатели на объявленные объекты или объекты, для которых выделена память), обрабатываются так же, как наследованные безопасно.

`preferred` — как и раньше, но указатели, наследованные небезопасно, не должны разыменовываться.

`strict` — указатели, наследованные небезопасно, могут обрабатываться не так, как наследованные безопасно.
