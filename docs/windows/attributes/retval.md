---
description: 'Дополнительные сведения о: retval'
title: retval (атрибут COM C++)
ms.date: 10/02/2018
f1_keywords:
- vc-attr.retval
helpviewer_keywords:
- retval attribute
ms.assetid: bfa16f08-157d-4eea-afde-1232c54b8501
ms.openlocfilehash: 15bfc994d18a9c61c37402aa763ecbfd96cbd768
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97114862"
---
# <a name="retval"></a>retval

Определяет параметр, который получает возвращаемое значение элемента.

## <a name="syntax"></a>Синтаксис

```cpp
[retval]
```

## <a name="remarks"></a>Remarks

Атрибут **retval** C++ имеет те же функциональные возможности, что и атрибут [retval](/windows/win32/Midl/retval) в формате MIDL.

значение **retval** должно присутствовать в последнем аргументе в объявлении функции.

## <a name="example"></a>Пример

См. пример для [привязки](bindable.md) к примеру использования параметра **retval**.

## <a name="requirements"></a>Требования

| Контекст атрибута | Значение |
|-|-|
|**Относится к**|Параметр интерфейса, метод интерфейса|
|**REPEATABLE**|Нет|
|**Требуемые атрибуты**|**out**|
|**Недопустимые атрибуты**|**in**|

Дополнительные сведения о контекстах атрибутов см. в разделе [Контексты атрибутов](cpp-attributes-com-net.md#contexts).

## <a name="see-also"></a>См. также раздел

[Атрибуты IDL](idl-attributes.md)<br/>
[Атрибуты параметра](parameter-attributes.md)<br/>
[Атрибуты метода](method-attributes.md)
