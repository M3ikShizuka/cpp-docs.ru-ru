---
description: 'Дополнительные сведения: switch_type'
title: switch_type (атрибут COM C++)
ms.date: 10/02/2018
f1_keywords:
- vc-attr.switch_type
helpviewer_keywords:
- switch_type attribute
ms.assetid: e24544dc-b3bc-48ae-b249-f967db49271e
ms.openlocfilehash: e291524d00afff89aa17634307426ef62cd40f4b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97327264"
---
# <a name="switch_type"></a>switch_type

Определяет тип переменной, используемой в качестве discriminant объединения.

## <a name="syntax"></a>Синтаксис

```cpp
[switch_type(
type
}]
```

### <a name="parameters"></a>Параметры

*type*<br/>
Тип переключателя может быть целым числом, символом, логическим значением или типом перечисления.

## <a name="remarks"></a>Комментарии

Атрибут **switch_type** C++ имеет те же функциональные возможности, что и атрибут [switch_type](/windows/win32/Midl/switch-type) MIDL.

Атрибуты C++ не поддерживают [инкапсулированные объединения](/windows/win32/Midl/encapsulated-unions). [Неинкапсулированные объединения](/windows/win32/Midl/nonencapsulated-unions) поддерживаются только в следующей форме:

```cpp
// cpp_attr_ref_switch_type.cpp
// compile with: /LD
#include <windows.h>
[module(name="MyLibrary")];
[ export ]
struct SizedValue2 {
   [switch_type("char"), switch_is(kind)] union {
      [case(1), string]
         wchar_t* wval;
      [default, string]
         char* val;
   };
   char kind;
};
```

## <a name="example"></a>Пример

Пример использования **switch_type** см. в примере [варианта](case-cpp.md) .

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
[программе](export.md)
