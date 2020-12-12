---
description: 'Дополнительные сведения: size_is'
title: size_is (атрибут COM C++)
ms.date: 10/02/2018
f1_keywords:
- vc-attr.size_is
helpviewer_keywords:
- size_is attribute
ms.assetid: 70192d09-f6c5-4d52-b3fe-303f8cb10aa5
ms.openlocfilehash: f61124dc286de1c8893f093454c921b4d6e46037
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97329604"
---
# <a name="size_is"></a>size_is

Укажите размер памяти, выделенной для указателей размера, размеры указателей для указателей размеров, а также однокомпонентные или многомерные массивы.

## <a name="syntax"></a>Синтаксис

```cpp
[ size_is("expression") ]
```

### <a name="parameters"></a>Параметры

*expression*<br/>
Размер памяти, выделенной для указателей размера.

## <a name="remarks"></a>Комментарии

Атрибут **size_is** C++ имеет те же функциональные возможности, что и атрибут [size_is](/windows/win32/Midl/size-is) MIDL.

## <a name="example"></a>Пример

Пример указания раздела массива см. в примере для [first_is](first-is.md) .

## <a name="requirements"></a>Требования

| Контекст атрибута | Значение |
|-|-|
|**Относится к**|Поле в **`struct`** или **`union`** , параметр интерфейса, метод интерфейса|
|**REPEATABLE**|Нет|
|**Требуемые атрибуты**|Нет|
|**Недопустимые атрибуты**|`max_is`|

Дополнительные сведения о контекстах атрибутов см. в разделе [Контексты атрибутов](cpp-attributes-com-net.md#contexts).

## <a name="see-also"></a>См. также раздел

[Атрибуты IDL](idl-attributes.md)<br/>
[Атрибуты typedef, enum, Union и struct](typedef-enum-union-and-struct-attributes.md)<br/>
[Атрибуты параметра](parameter-attributes.md)<br/>
[first_is](first-is.md)<br/>
[last_is](last-is.md)<br/>
[max_is](max-is.md)<br/>
[length_is](length-is.md)
