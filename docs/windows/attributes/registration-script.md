---
description: 'Дополнительные сведения: registration_script'
title: registration_script (атрибут COM C++)
ms.date: 10/02/2018
f1_keywords:
- vc-attr.registration_script
helpviewer_keywords:
- registration_script attribute
ms.assetid: 786f8072-9187-4163-a979-7a604dd4c888
ms.openlocfilehash: 3722a799818c8ad76d710e4c570bc5fdd6b2e10c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97327337"
---
# <a name="registration_script"></a>registration_script

Выполняет указанный пользовательский скрипт регистрации.

## <a name="syntax"></a>Синтаксис

```cpp
[ registration_script(script) ]
```

### <a name="parameters"></a>Параметры

*script*<br/>
Полный путь к файлу пользовательского скрипта регистрации (RGS). Значение **None**, например `script = "none"` , указывает, что компонент coclass не имеет требований регистрации.

## <a name="remarks"></a>Комментарии

Атрибут **registration_script** C++ выполняет пользовательский скрипт регистрации, указанный в *скрипте*. Если этот атрибут не указан, используется стандартный RGS-файл (содержащий сведения для регистрации компонента). Дополнительные сведения о RGS-файлах см. [в разделе "компонент реестра ATL" (регистратор)](../../atl/atl-registry-component-registrar.md).

Этот атрибут требует, чтобы атрибут [coclass](coclass.md), [progid](progid.md)или [vi_progid](vi-progid.md) (или другой атрибут, который подразумевает один из них) также применялся к этому элементу.

## <a name="example"></a>Пример

Следующий код указывает, что у компонента есть сценарий реестра с именем cpp_attr_ref_registration_script. RGS.

```cpp
// cpp_attr_ref_registration_script.cpp
// compile with: /LD
#define _ATL_ATTRIBUTES
#include "atlbase.h"
#include "atlcom.h"

[module (name="REG")];

[object, uuid("d9cd196b-6836-470b-9b9b-5b04b828e5b0")]
__interface IFace {};

// requires "cpp_attr_ref_registration_script.rgs"
// create sample .RGS file "cpp_attr_ref_registration_script.rgs" if it does not exist
[ coclass, registration_script(script="cpp_attr_ref_registration_script.rgs"),
  uuid("50d3ad42-3601-4f26-8cfe-0f1f26f98f67")]
class CMyClass:public IFace {};
```

## <a name="requirements"></a>Требования

| Контекст атрибута | Значение |
|-|-|
|**Относится к**|**`class`**, **`struct`**|
|**REPEATABLE**|Нет|
|**Требуемые атрибуты**|Один или несколько из следующих элементов: `coclass` , `progid` или `vi_progid` .|
|**Недопустимые атрибуты**|Нет|

Дополнительные сведения о контекстах атрибутов см. в разделе [Контексты атрибутов](cpp-attributes-com-net.md#contexts).

## <a name="see-also"></a>См. также раздел

[Атрибуты COM](com-attributes.md)<br/>
[Атрибуты класса](class-attributes.md)<br/>
[RDX](rdx.md)
