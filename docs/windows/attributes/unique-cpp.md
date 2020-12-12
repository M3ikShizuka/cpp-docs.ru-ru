---
description: 'Дополнительные сведения: уникальные (C++)'
title: уникальный (атрибут COM C++)
ms.date: 10/02/2018
f1_keywords:
- vc-attr.unique
helpviewer_keywords:
- unique attribute
ms.assetid: abd7ed14-5ae7-44a8-8333-0058e9c92b2f
ms.openlocfilehash: 46db247e5e2106821fb3ab36746c1586409388ee
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97118320"
---
# <a name="unique-c"></a>unique (C++)

Задает уникальный указатель.

## <a name="syntax"></a>Синтаксис

```cpp
[unique]
```

## <a name="remarks"></a>Remarks

**Уникальный** атрибут C++ имеет те же функциональные возможности, что и [уникальный](/windows/win32/Midl/unique) атрибут MIDL.

## <a name="example"></a>Пример

Пример использования **UNIQUE** см. в примере [ref](ref-cpp.md) .

## <a name="requirements"></a>Требования

| Контекст атрибута | Значение |
|-|-|
|**Относится к**|**`typedef`**, **`struct`** , **`union`** , параметр интерфейса, метод интерфейса|
|**REPEATABLE**|Нет|
|**Требуемые атрибуты**|Нет|
|**Недопустимые атрибуты**|Нет|

Дополнительные сведения о контекстах атрибутов см. в разделе [Контексты атрибутов](cpp-attributes-com-net.md#contexts).

## <a name="see-also"></a>См. также раздел

[Атрибуты IDL](idl-attributes.md)<br/>
[Атрибуты typedef, enum, Union и struct](typedef-enum-union-and-struct-attributes.md)<br/>
[Атрибуты параметра](parameter-attributes.md)
