---
description: 'Дополнительные сведения: Custom (C++)'
title: custom (C++)
ms.date: 11/04/2016
f1_keywords:
- vc-attr.custom
helpviewer_keywords:
- custom attributes, defining
ms.assetid: 3abac928-4d55-4ea6-8cf6-8427a4ad79f1
ms.openlocfilehash: 7771230fd6eed5f567fb2e74e8cd869a0b3618f0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97333151"
---
# <a name="custom-c"></a>custom (C++)

Определяет метаданные для объекта в библиотеке типов.

## <a name="syntax"></a>Синтаксис

```cpp
[ custom(
   uuid,
   value
) ];
```

### <a name="parameters"></a>Параметры

*uuid*<br/>
Уникальный идентификатор.

*value*<br/>
Значение, которое может быть помещается в вариант.

## <a name="remarks"></a>Комментарии

**Настраиваемый** атрибут C++ приведет к помещению данных в библиотеку типов. Вам потребуется средство, считывающее пользовательское значение из библиотеки типов.

**Пользовательский** атрибут имеет те же функциональные возможности, что и [Пользовательский](/windows/win32/Midl/custom) атрибут MIDL.

## <a name="requirements"></a>Требования

### <a name="attribute-context"></a>Контекст атрибута

- **Применимо к**: не com `interface` , `idl_module` методы, члены интерфейса, параметры интерфейса,,,, **`typedef`** **`class`** **`enum`** **`union`** и **`struct`** типы.
- **REPEATABLE**: Да.
- **Обязательные атрибуты**: **coclass** (при использовании в классе).
- **Недопустимые атрибуты**: нет.

Дополнительные сведения о контекстах атрибутов см. в разделе [Контексты атрибутов](cpp-attributes-com-net.md#contexts).

## <a name="see-also"></a>См. также раздел

[Атрибуты IDL](idl-attributes.md)<br/>
[Изолированные атрибуты](stand-alone-attributes.md)<br/>
[Атрибуты typedef, enum, Union и struct](typedef-enum-union-and-struct-attributes.md)<br/>
[Атрибуты параметра](parameter-attributes.md)<br/>
[Атрибуты метода](method-attributes.md)<br/>
[Атрибуты класса](class-attributes.md)<br/>
[Атрибуты интерфейса](interface-attributes.md)
