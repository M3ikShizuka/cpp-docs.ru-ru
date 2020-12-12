---
description: 'Дополнительные сведения: pointer_default'
title: pointer_default (атрибут COM C++)
ms.date: 10/02/2018
f1_keywords:
- vc-attr.pointer_default
helpviewer_keywords:
- pointer_default attribute
ms.assetid: 2d0c7bbc-a1e8-4337-9e54-e304523e2735
ms.openlocfilehash: 0c7768227a5922bca7e1b48b3ad82821bb62ea54
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97329683"
---
# <a name="pointer_default"></a>pointer_default

Задает атрибут указателя по умолчанию для всех указателей, за исключением указателей верхнего уровня, которые отображаются в списках параметров.

## <a name="syntax"></a>Синтаксис

```cpp
[ pointer_default(value) ]
```

### <a name="parameters"></a>Параметры

*value*<br/>
Значение типа, описывающее тип указателя: **ptr**, **ref** или **UNIQUE**.

## <a name="remarks"></a>Комментарии

Атрибут **pointer_default** C++ имеет те же функциональные возможности, что и атрибут [pointer_default](/windows/win32/Midl/pointer-default) MIDL.

## <a name="example"></a>Пример

См. пример для [DefaultValue](defaultvalue.md) для примера использования **pointer_default**.

## <a name="requirements"></a>Требования

| Контекст атрибута | Значение |
|-|-|
|**Относится к**|**interface**|
|**REPEATABLE**|Нет|
|**Требуемые атрибуты**|Нет|
|**Недопустимые атрибуты**|Нет|

Дополнительные сведения о контекстах атрибутов см. в разделе [Контексты атрибутов](cpp-attributes-com-net.md#contexts).

## <a name="see-also"></a>См. также раздел

[Атрибуты IDL](idl-attributes.md)<br/>
[Атрибуты интерфейса](interface-attributes.md)
