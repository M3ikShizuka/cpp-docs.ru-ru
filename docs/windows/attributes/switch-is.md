---
description: 'Дополнительные сведения: switch_is'
title: switch_is (атрибут COM C++)
ms.date: 10/02/2018
f1_keywords:
- vc-attr.switch_is
helpviewer_keywords:
- switch_is attribute
ms.assetid: f1fffe5d-12d2-4e0f-8803-ccb715177d2d
ms.openlocfilehash: 88489a9722e79da6629dfc2b39bfbe7f6ab39932
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97329562"
---
# <a name="switch_is"></a>switch_is

Указывает выражение или идентификатор, выступающий в качестве discriminant объединения, который выбирает элемент объединения.

## <a name="syntax"></a>Синтаксис

```cpp
[switch_is]
```

## <a name="remarks"></a>Remarks

Атрибут **switch_is** C++ имеет те же функциональные возможности, что и атрибут [switch_is](/windows/win32/Midl/switch-is) MIDL.

## <a name="example"></a>Пример

Пример использования **switch_is** см. в примере [варианта](case-cpp.md) .

## <a name="requirements"></a>Требования

| Контекст атрибута | Значение |
|-|-|
|**Относится к**|**`typedef`**|
|**REPEATABLE**|Нет|
|**Требуемые атрибуты**|Нет|
|**Недопустимые атрибуты**|Нет|

Дополнительные сведения о контекстах атрибутов см. в разделе [Контексты атрибутов](cpp-attributes-com-net.md#contexts).

## <a name="see-also"></a>См. также раздел

[Атрибуты IDL](idl-attributes.md)<br/>
[Атрибуты typedef, enum, Union и struct](typedef-enum-union-and-struct-attributes.md)<br/>
[switch_type](switch-type.md)
