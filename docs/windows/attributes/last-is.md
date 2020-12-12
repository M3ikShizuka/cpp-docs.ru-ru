---
description: 'Дополнительные сведения: last_is'
title: last_is (атрибут COM C++)
ms.date: 10/02/2018
f1_keywords:
- vc-attr.last_is
helpviewer_keywords:
- last_is attribute
ms.assetid: 9e045ac0-fa38-4249-af55-67bde5d0a58c
ms.openlocfilehash: 41f436d1cd4317385d702d8763d69e6df7d07849
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97327541"
---
# <a name="last_is"></a>last_is

Задает индекс последнего передаваемого элемента массива.

## <a name="syntax"></a>Синтаксис

```cpp
[ last_is("expression") ]
```

### <a name="parameters"></a>Параметры

*expression*<br/>
Одно или несколько выражений языка C. Пустые слоты аргументов разрешены.

## <a name="remarks"></a>Комментарии

Атрибут **last_is** C++ имеет те же функциональные возможности, что и атрибут [last_is](/windows/win32/Midl/last-is) MIDL.

## <a name="example"></a>Пример

Пример указания раздела массива см. в разделе [first_is](first-is.md) .

## <a name="requirements"></a>Требования

| Контекст атрибута | Значение |
|-|-|
|**Относится к**|Поле в **`struct`** или **`union`** , параметр интерфейса, метод интерфейса|
|**REPEATABLE**|Нет|
|**Требуемые атрибуты**|Нет|
|**Недопустимые атрибуты**|Нет|

Дополнительные сведения см. в разделе [Контексты атрибутов](cpp-attributes-com-net.md#contexts).

## <a name="see-also"></a>См. также раздел

[Атрибуты IDL](idl-attributes.md)<br/>
[Атрибуты typedef, enum, Union и struct](typedef-enum-union-and-struct-attributes.md)<br/>
[Атрибуты параметра](parameter-attributes.md)<br/>
[first_is](first-is.md)<br/>
[max_is](max-is.md)<br/>
[length_is](length-is.md)<br/>
[size_is](size-is.md)
