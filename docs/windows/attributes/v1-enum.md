---
description: 'Дополнительные сведения: v1_enum'
title: v1_enum (атрибут COM C++)
ms.date: 10/02/2018
f1_keywords:
- vc-attr.v1_enum
helpviewer_keywords:
- v1_enum attribute
ms.assetid: 2fe92d92-81b9-4a1c-b6ce-437d0eb770ca
ms.openlocfilehash: c096ec78971e8980b68572c7f0bbb4510d03d3d1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97327204"
---
# <a name="v1_enum"></a>v1_enum

Указывает, что указанный перечисляемый тип передается как 32-разрядная сущность, а не как 16-разрядное значение по умолчанию.

## <a name="syntax"></a>Синтаксис

```cpp
[v1_enum]
```

## <a name="remarks"></a>Remarks

Атрибут **v1_enum** C++ имеет те же функциональные возможности, что и атрибут [v1_enum](/windows/win32/Midl/v1-enum) MIDL.

## <a name="example"></a>Пример

В следующем коде показано использование **v1_enum**.

```cpp
// cpp_attr_ref_v1_enum.cpp
// compile with: /LD
[module(name="MyLibrary")];

[export, v1_enum]
enum eList {
   e1 = 1, e2 = 2
};
```

## <a name="requirements"></a>Требования

| Контекст атрибута | Значение |
|-|-|
|**Относится к**|Перечисляемый тип|
|**REPEATABLE**|Нет|
|**Требуемые атрибуты**|Нет|
|**Недопустимые атрибуты**|Нет|

Дополнительные сведения о контекстах атрибутов см. в разделе [Контексты атрибутов](cpp-attributes-com-net.md#contexts).

## <a name="see-also"></a>См. также раздел

[Атрибуты IDL](idl-attributes.md)<br/>
[Атрибуты typedef, enum, Union и struct](typedef-enum-union-and-struct-attributes.md)
