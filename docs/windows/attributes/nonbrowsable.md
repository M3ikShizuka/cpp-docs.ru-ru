---
description: Дополнительные сведения о неотображаемых
title: недоступный для просмотра (атрибут COM C++)
ms.date: 10/02/2018
f1_keywords:
- vc-attr.nonbrowsable
helpviewer_keywords:
- nonbrowsable attribute
ms.assetid: e71a98e7-4b65-454a-9829-342b9f2a84be
ms.openlocfilehash: 943458ff989a3f00d2ce33a4f5681a8bd29a76ca
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97329766"
---
# <a name="nonbrowsable"></a>nonbrowsable

Указывает, что член интерфейса не должен отображаться в обозревателе свойств.

## <a name="syntax"></a>Синтаксис

```cpp
[nonbrowsable]
```

## <a name="remarks"></a>Remarks

**Неотображаемый** атрибут C++ имеет те же функциональные возможности, что и [неотображаемый](/windows/win32/Midl/nonbrowsable) атрибут MIDL.

## <a name="example"></a>Пример

```cpp
// cpp_attr_ref_nonbrowsable.cpp
// compile with: /LD
#include <unknwn.h>
[module(name="MyLib")];

[object, helpstring("help string"), helpstringcontext(1),
uuid="11111111-1111-1111-1111-111111111111"]
__interface IMyI
{
   [nonbrowsable] HRESULT xx();
};
```

## <a name="requirements"></a>Требования

| Контекст атрибута | Значение |
|-|-|
|**Относится к**|Метод интерфейса|
|**REPEATABLE**|Нет|
|**Требуемые атрибуты**|Нет|
|**Недопустимые атрибуты**|Нет|

Дополнительные сведения о контекстах атрибутов см. в разделе [Контексты атрибутов](cpp-attributes-com-net.md#contexts).

## <a name="see-also"></a>См. также раздел

[Атрибуты IDL](idl-attributes.md)<br/>
[Атрибуты метода](method-attributes.md)
