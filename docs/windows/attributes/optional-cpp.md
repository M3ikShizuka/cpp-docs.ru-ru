---
description: 'Дополнительные сведения о: необязательно (C++)'
title: необязательно (атрибут COM C++)
ms.date: 10/02/2018
f1_keywords:
- vc-attr.optional
helpviewer_keywords:
- optional attribute
ms.assetid: 86656a66-8e11-4589-8e30-9b0f34eeed03
ms.openlocfilehash: 70ae49854a496aad35edc87bdd1ac5facb899448
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97329728"
---
# <a name="optional-c"></a>optional (C++)

Задает необязательный параметр для функции-члена.

## <a name="syntax"></a>Синтаксис

```cpp
[optional]
```

## <a name="remarks"></a>Remarks

**Необязательный** атрибут C++ имеет те же функциональные возможности, что и [необязательный](/windows/win32/Midl/optional) атрибут MIDL.

## <a name="example"></a>Пример

В следующем коде показано, как можно использовать параметр **Optional** :

```cpp
// cpp_attr_ref_optional.cpp
// compile with: /LD
#include "unknwn.h"
[module(name="ATLFIRELib")];

[dispinterface, uuid("00000000-0000-0000-0000-000000000001")]
__interface IFireTabCtrl : IDispatch
{
   [id(1)] long procedure ([in, optional] VARIANT i);
};
```

## <a name="requirements"></a>Требования

| Контекст атрибута | Значение |
|-|-|
|**Относится к**|Параметр интерфейса|
|**REPEATABLE**|Нет|
|**Требуемые атрибуты**|Нет|
|**Недопустимые атрибуты**|Нет|

Дополнительные сведения о контекстах атрибутов см. в разделе [Контексты атрибутов](cpp-attributes-com-net.md#contexts).

## <a name="see-also"></a>См. также раздел

[Атрибуты IDL](idl-attributes.md)<br/>
[Атрибуты параметра](parameter-attributes.md)
