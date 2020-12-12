---
description: 'Дополнительные сведения о: ID'
title: ID (атрибут COM C++)
ms.date: 10/02/2018
f1_keywords:
- vc-attr.id
helpviewer_keywords:
- id attribute
ms.assetid: a48d2c99-c5d2-4f46-bf96-5ac88dcb5d0c
ms.openlocfilehash: 04f7144e1c6f8b6655b0b6be23e0ffa4f22dc27c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97180205"
---
# <a name="id"></a>идентификатор

Задает параметр *DISPID* для функции-члена (свойства или метода в интерфейсе или DISP).

## <a name="syntax"></a>Синтаксис

```cpp
[ id(dispid) ]
```

### <a name="parameters"></a>Параметры

*DISPID*<br/>
Идентификатор диспетчеризации для метода интерфейса.

## <a name="remarks"></a>Комментарии

Атрибут **ID** C++ имеет те же функциональные возможности, что и атрибут [ID](/windows/win32/Midl/id) MIDL.

## <a name="example"></a>Пример

Пример использования **идентификатора** см. в примере для [привязки](bindable.md) .

## <a name="requirements"></a>Требования

| Контекст атрибута | Значение |
|-|-|
|**Относится к**|Метод интерфейса|
|**REPEATABLE**|Нет|
|**Требуемые атрибуты**|Нет|
|**Недопустимые атрибуты**|Нет|

Дополнительные сведения см. в разделе [Контексты атрибутов](cpp-attributes-com-net.md#contexts).

## <a name="see-also"></a>См. также раздел

[Атрибуты IDL](idl-attributes.md)<br/>
[Атрибуты метода](method-attributes.md)<br/>
[Атрибуты элементов данных](data-member-attributes.md)<br/>
[максимально](defaultvalue.md)<br/>
[in](in-cpp.md)<br/>
[out](out-cpp.md)
