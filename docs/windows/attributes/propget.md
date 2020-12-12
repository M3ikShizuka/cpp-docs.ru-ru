---
description: 'Дополнительные сведения о: propget'
title: propget (атрибут COM C++)
ms.date: 10/02/2018
f1_keywords:
- vc-attr.propget
helpviewer_keywords:
- propget attribute
ms.assetid: c9d4a97f-36dd-4b61-8eb0-b1a217598f14
ms.openlocfilehash: 9fe284fb35d4753fbc3e124458200a9882838450
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97327402"
---
# <a name="propget"></a>propget

Задает функцию доступа к свойству.

## <a name="syntax"></a>Синтаксис

```cpp
[propget]
```

## <a name="remarks"></a>Remarks

Атрибут **propget** C++ имеет те же функциональные возможности, что и атрибуту MIDL для [propget](/windows/win32/Midl/propget) .

## <a name="example"></a>Пример

См. пример для [привязки](bindable.md) к примеру использования **propget**.

## <a name="requirements"></a>Требования

| Контекст атрибута | Значение |
|-|-|
|**Относится к**|Метод|
|**REPEATABLE**|Нет|
|**Требуемые атрибуты**|Нет|
|**Недопустимые атрибуты**|`propput`, `propputref`|

Дополнительные сведения о контекстах атрибутов см. в разделе [Контексты атрибутов](cpp-attributes-com-net.md#contexts).

## <a name="see-also"></a>См. также раздел

[Атрибуты IDL](idl-attributes.md)<br/>
[Атрибуты метода](method-attributes.md)<br/>
[propput](propput.md)<br/>
[propputref](propputref.md)
