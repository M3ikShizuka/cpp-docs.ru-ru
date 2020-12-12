---
description: 'Дополнительные сведения: PTR'
title: PTR (атрибут COM C++)
ms.date: 10/02/2018
f1_keywords:
- vc-attr.ptr
helpviewer_keywords:
- ptr attribute
ms.assetid: 95eaea57-a5be-45f6-a612-ba2c9bc4645a
ms.openlocfilehash: 0e1a08ec51cbb2e6ca5dc469fb359da775141a2b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97327367"
---
# <a name="ptr"></a>ptr

Назначает указатель в качестве полного указателя.

## <a name="syntax"></a>Синтаксис

```cpp
[ptr]
```

## <a name="remarks"></a>Remarks

Атрибут **ptr** C++ имеет те же функциональные возможности, что и атрибут [ptr](/windows/win32/Midl/ptr) MIDL.

## <a name="example"></a>Пример

См. пример для [DefaultValue](defaultvalue.md) для примера использования **ptr**.

## <a name="requirements"></a>Требования

| Контекст атрибута | Значение |
|-|-|
|**Относится к**|Параметр интерфейса, метод интерфейса, **`typedef`**|
|**REPEATABLE**|Нет|
|**Требуемые атрибуты**|Нет|
|**Недопустимые атрибуты**|Нет|

Дополнительные сведения о контекстах атрибутов см. в разделе [Контексты атрибутов](cpp-attributes-com-net.md#contexts).

## <a name="see-also"></a>См. также раздел

[Атрибуты IDL](idl-attributes.md)<br/>
[Атрибуты интерфейса](interface-attributes.md)<br/>
[Атрибуты метода](method-attributes.md)<br/>
[Атрибуты typedef, enum, Union и struct](typedef-enum-union-and-struct-attributes.md)
