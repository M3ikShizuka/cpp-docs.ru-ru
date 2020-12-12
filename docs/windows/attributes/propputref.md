---
description: 'Дополнительные сведения о: propputref'
title: propputref (атрибут COM C++)
ms.date: 10/02/2018
f1_keywords:
- vc-attr.propputref
helpviewer_keywords:
- propputref attribute
ms.assetid: 9b0aed74-fdc7-4e59-9117-949bea4f86dd
ms.openlocfilehash: 5f09d742ef0df75df03e4f4d740181cfcaaa8f2d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97329672"
---
# <a name="propputref"></a>propputref

Задает функцию настройки свойства, которая использует ссылку вместо значения.

## <a name="syntax"></a>Синтаксис

```cpp
[propputref]
```

## <a name="remarks"></a>Remarks

Атрибут **propputref** C++ имеет те же функциональные возможности, что и атрибут [propputref](/windows/win32/Midl/propputref) MIDL.

## <a name="example"></a>Пример

Пример использования **propputref** см. в примере для [привязки](bindable.md) .

## <a name="requirements"></a>Требования

| Контекст атрибута | Значение |
|-|-|
|**Относится к**|Метод|
|**REPEATABLE**|Нет|
|**Требуемые атрибуты**|Нет|
|**Недопустимые атрибуты**|`propget`, `propput`|

Дополнительные сведения о контекстах атрибутов см. в разделе [Контексты атрибутов](cpp-attributes-com-net.md#contexts).

## <a name="see-also"></a>См. также раздел

[Атрибуты IDL](idl-attributes.md)<br/>
[Атрибуты метода](method-attributes.md)<br/>
[propget](propget.md)<br/>
[propput](propput.md)
