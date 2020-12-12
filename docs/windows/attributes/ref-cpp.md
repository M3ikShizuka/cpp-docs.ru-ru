---
description: 'Дополнительные сведения: ref (C++)'
title: ref (атрибут COM C++)
ms.date: 10/02/2018
f1_keywords:
- vc-attr.ref
helpviewer_keywords:
- ref attribute
ms.assetid: 67e82d3e-07d9-4ef8-bf2b-0a4491d12557
ms.openlocfilehash: 2ddfafee97f0b8b6a8c35fdff8664335ba6aa10d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97114927"
---
# <a name="ref-c"></a>ref (C++)

Определяет указатель ссылки.

## <a name="syntax"></a>Синтаксис

```cpp
[ref]
```

## <a name="remarks"></a>Remarks

Атрибут **ref** C++ имеет те же функциональные возможности, что и атрибут [ref](/windows/win32/Midl/ref) MIDL.

## <a name="example"></a>Пример

В следующем коде показано, как использовать атрибут **ref** :

```cpp
// cpp_attr_ref_ref.cpp
// compile with: /LD
#include <windows.h>
[module(name="ATLFIRELib")];
[dispinterface, uuid("00000000-0000-0000-0000-000000000001")]
__interface IFireTabCtrl
{
   [id(1), unique] char * GetFirstName([in, ref] char * pszFullName );
};
```

## <a name="requirements"></a>Требования

| Контекст атрибута | Значение |
|-|-|
|**Относится к**|**`typedef`**, параметр интерфейса, метод интерфейса|
|**REPEATABLE**|Нет|
|**Требуемые атрибуты**|Нет|
|**Недопустимые атрибуты**|Нет|

Дополнительные сведения о контекстах атрибутов см. в разделе [Контексты атрибутов](cpp-attributes-com-net.md#contexts).

## <a name="see-also"></a>См. также раздел

[Атрибуты IDL](idl-attributes.md)<br/>
[Атрибуты typedef, enum, Union и struct](typedef-enum-union-and-struct-attributes.md)<br/>
[Атрибуты параметра](parameter-attributes.md)
