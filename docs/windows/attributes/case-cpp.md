---
description: 'Дополнительные сведения: Case (C++)'
title: Case (атрибут COM C++)
ms.date: 10/02/2018
f1_keywords:
- vc-attr.case
helpviewer_keywords:
- case attribute
ms.assetid: 6fb883c3-0526-4932-a901-b4564dcaeb7d
ms.openlocfilehash: d851e662387425ca94cc6a03877babf011c7028b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97247440"
---
# <a name="case-c"></a>case (C++)

Используется с атрибутом [switch_type](switch-type.md) в **`union`** .

## <a name="syntax"></a>Синтаксис

```cpp
[ case(value) ]
```

#### <a name="parameters"></a>Параметры

*value*<br/>
Возможное входное значение, для которого необходимо обеспечить обработку. Тип **значения** может быть одним из следующих типов:

- **`int`**

- **`char`**

- `boolean`

- **`enum`**

или идентификатор такого типа.

## <a name="remarks"></a>Комментарии

Атрибут **case** C++ имеет те же функциональные возможности, что **и атрибут MIDL.** Этот атрибут используется только с атрибутом [switch_type](switch-type.md) .

## <a name="example"></a>Пример

В следующем коде показано использование атрибута **case** :

```cpp
// cpp_attr_ref_case.cpp
// compile with: /LD
#include <unknwn.h>
[export]
struct SizedValue2 {
   [switch_type(char), switch_is(kind)] union {
      [case(1), string]
          wchar_t* wval;
      [default, string]
          char* val;
   };
    char kind;
};
[module(name="ATLFIRELib")];
```

## <a name="requirements"></a>Требования

| Контекст атрибута | Значение |
|-|-|
|**Относится к**|Член **`class`** или **`struct`**|
|**REPEATABLE**|Нет|
|**Требуемые атрибуты**|Нет|
|**Недопустимые атрибуты**|Нет|

Дополнительные сведения о контекстах атрибутов см. в разделе [Контексты атрибутов](cpp-attributes-com-net.md#contexts).

## <a name="see-also"></a>См. также раздел

[Атрибуты IDL](idl-attributes.md)<br/>
[Атрибуты typedef, enum, Union и struct](typedef-enum-union-and-struct-attributes.md)<br/>
[Атрибуты класса](class-attributes.md)
