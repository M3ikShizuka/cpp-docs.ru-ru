---
description: 'Дополнительные сведения: Virtual (C++)'
title: virtual (C++)
ms.date: 11/04/2016
f1_keywords:
- virtual_cpp
- virtual
helpviewer_keywords:
- virtual base classes [C++], declaring
- base classes [C++], virtual
- virtual functions [C++], declaring
- virtual keyword [C++]
ms.assetid: c2eb987d-6cf3-43b6-aa0c-29a6f561b1ae
ms.openlocfilehash: bf90baa1d9be9992e2e516743857bf8889087188
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97161354"
---
# <a name="virtual-c"></a>virtual (C++)

**`virtual`** Ключевое слово объявляет виртуальную функцию или виртуальный базовый класс.

## <a name="syntax"></a>Синтаксис

```
virtual [type-specifiers] member-function-declarator
virtual [access-specifier] base-class-name
```

#### <a name="parameters"></a>Параметры

*описатели типа*<br/>
Указывает тип возвращаемого значения виртуальной функции-члена.

*декларатор с функцией-членом*<br/>
Объявляет функцию-член.

*описатель доступа*<br/>
Определяет уровень доступа к базовому классу, **`public`** **`protected`** или **`private`** . Может использоваться до или после **`virtual`** ключевого слова.

*имя базового класса*<br/>
Определяет ранее объявленный тип класса.

## <a name="remarks"></a>Комментарии

Дополнительные сведения см. в разделе [виртуальные функции](../cpp/virtual-functions.md) .

Также см. следующие ключевые слова: [класс](../cpp/class-cpp.md), [частный](../cpp/private-cpp.md), [открытый](../cpp/public-cpp.md)и [защищенный](../cpp/protected-cpp.md).

## <a name="see-also"></a>См. также раздел

[Ключевые слова](../cpp/keywords-cpp.md)
