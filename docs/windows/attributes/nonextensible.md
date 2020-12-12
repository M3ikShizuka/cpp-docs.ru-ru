---
description: 'Дополнительные сведения: нерасширяемые'
title: нерасширяемый (атрибут COM C++)
ms.date: 10/02/2018
f1_keywords:
- vc-attr.nonextensible
helpviewer_keywords:
- nonextensible attribute
ms.assetid: c7ef1554-809f-4ea0-a7cd-dc7786d40c3e
ms.openlocfilehash: dfb0eda0fc8c6de367ee29ec3786750ba40395ec
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97327445"
---
# <a name="nonextensible"></a>nonextensible

Указывает, что `IDispatch` Реализация включает только свойства и методы, перечисленные в описании интерфейса, и не может быть расширена с помощью дополнительных элементов во время выполнения.

## <a name="syntax"></a>Синтаксис

```cpp
[nonextensible]
```

## <a name="remarks"></a>Remarks

**Нерасширяемый** атрибут C++ имеет те же функциональные возможности, что и [нерасширяемый](/windows/win32/Midl/nonextensible) атрибут MIDL.

Для использования **нерасширяемости** также требуется атрибут [oleautomation](oleautomation.md) .

## <a name="example"></a>Пример

В следующем коде показано одно использование **нерасширяемого** атрибута:

```cpp
// cpp_attr_ref_nonextensible.cpp
// compile with: /LD
#include "unknwn.h"
[module(name="ATLFIRELib")];
[export] typedef long HRESULT;

[dual, nonextensible, ms_union, oleautomation,
uuid("00000000-0000-0000-0000-000000000001")]
__interface IFireTabCtrl
{
   HRESULT procedure (int i);
};
```

## <a name="requirements"></a>Требования

| Контекст атрибута | Значение |
|-|-|
|**Относится к**|**interface**|
|**REPEATABLE**|Нет|
|**Требуемые атрибуты**|`dual` и `oleautomation` , или `dispinterface`|
|**Недопустимые атрибуты**|Нет|

Дополнительные сведения о контекстах атрибутов см. в разделе [Контексты атрибутов](cpp-attributes-com-net.md#contexts).

## <a name="see-also"></a>См. также раздел

[Атрибуты IDL](idl-attributes.md)<br/>
[Атрибуты интерфейса](interface-attributes.md)
