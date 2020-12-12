---
description: 'Дополнительные сведения о: ODL'
title: ODL (атрибут COM C++)
ms.date: 10/02/2018
f1_keywords:
- vc-attr.odl
helpviewer_keywords:
- odl attribute
ms.assetid: 75dcb314-b50f-4a63-9180-507ac1bc78f3
ms.openlocfilehash: 00228a11876a551a02a292fc4f20ea67f55506c2
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97329745"
---
# <a name="odl"></a>odl

Определяет интерфейс в виде интерфейса языка описания объектов (ODL). Компилятор MIDL не требует наличия атрибута **ODL** ; он распознается только для обеспечения совместимости с более старыми файлами. ODL.

## <a name="syntax"></a>Синтаксис

```cpp
[odl]
```

## <a name="remarks"></a>Remarks

Атрибут **ODL** C++ имеет те же функциональные возможности, что и атрибут [ODL](/windows/win32/Midl/odl) MIDL.

## <a name="example"></a>Пример

```cpp
// cpp_attr_ref_odl.cpp
// compile with: /LD
#include <unknwn.h>
[module(name="MyLIb")];

[odl, oleautomation, dual, uuid("00000000-0000-0000-0000-000000000001")]
__interface IMyInterface
{
   HRESULT x();
};

[coclass, uuid("00000000-0000-0000-0000-000000000002")]
class cmyClass : public IMyInterface
{
public:
   HRESULT x(){}
};
```

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
