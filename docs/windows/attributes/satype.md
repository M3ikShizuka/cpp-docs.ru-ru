---
description: 'Дополнительные сведения о: сатипе'
title: сатипе (атрибут COM C++)
ms.date: 10/02/2018
f1_keywords:
- vc-attr.satype
helpviewer_keywords:
- satype attribute
ms.assetid: 1716590b-6bcb-4aba-b1bc-82f7335f02c3
ms.openlocfilehash: dab0f866eba5501a9a83d531d9cbdf50501dcff0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97327311"
---
# <a name="satype"></a>satype

Указывает тип данных `SAFEARRAY` структуры.

## <a name="syntax"></a>Синтаксис

```cpp
[ satype(data_type) ]
```

### <a name="parameters"></a>Параметры

*data_type*<br/>
Тип данных для `SAFEARRAY` структуры данных, передаваемой в качестве параметра в метод интерфейса.

## <a name="requirements"></a>Требования

| Контекст атрибута | Значение |
|-|-|
|**Относится к**|Параметр интерфейса, метод интерфейса|
|**REPEATABLE**|Нет|
|**Требуемые атрибуты**|Нет|
|**Недопустимые атрибуты**|None|

## <a name="remarks"></a>Remarks

Атрибут **сатипе** C++ задает тип данных `SAFEARRAY` .

> [!NOTE]
> Уровень косвенного обращения удаляется из `SAFEARRAY` указателя в созданном IDL-файле из того, как он объявлен в cpp-файле.

## <a name="example"></a>Пример

```cpp
// cpp_attr_ref_satype.cpp
// compile with: /LD
#include "unknwn.h"
[module(name="MyModule")];
[dispinterface, uuid("00000000-0000-0000-0000-000000000001")]
__interface A {
   [id(1)] HRESULT MyMethod ([in, satype("BSTR")] SAFEARRAY **p);
};
```

## <a name="see-also"></a>См. также раздел

[Атрибуты компилятора](compiler-attributes.md)<br/>
[Атрибуты параметра](parameter-attributes.md)<br/>
[Атрибуты метода](method-attributes.md)<br/>
[id](id.md)
