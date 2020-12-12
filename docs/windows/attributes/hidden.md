---
description: 'Дополнительные сведения о: Hidden'
title: Hidden (атрибут COM C++)
ms.date: 10/02/2018
f1_keywords:
- vc-attr.hidden
helpviewer_keywords:
- hidden attribute
ms.assetid: 199c96dd-fc07-46c7-af93-92020aebebe7
ms.openlocfilehash: 0609ef8b0dedb08e26e5442fd5070ca6a29e11d6
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97180231"
---
# <a name="hidden"></a>hidden

Указывает, что элемент существует, но не должен отображаться в браузере, ориентированном на пользователя.

## <a name="syntax"></a>Синтаксис

```cpp
[hidden]
```

## <a name="remarks"></a>Remarks

Атрибут **Hidden** C++ имеет те же функциональные возможности, что и [скрытый](/windows/win32/Midl/hidden) атрибут MIDL.

## <a name="example"></a>Пример

См. пример для [привязки](bindable.md) к примеру, как использовать **скрытый**.

## <a name="requirements"></a>Требования

| Контекст атрибута | Значение |
|-|-|
|**Относится к**|**интерфейс**, **`class`** , **`struct`** , метод, свойство|
|**REPEATABLE**|Нет|
|**Требуемые атрибуты**|**coclass** (при применении к **`class`** или **`struct`** )|
|**Недопустимые атрибуты**|Нет|

Дополнительные сведения см. в разделе [Контексты атрибутов](cpp-attributes-com-net.md#contexts).

## <a name="see-also"></a>См. также раздел

[Атрибуты IDL](idl-attributes.md)<br/>
[Атрибуты интерфейса](interface-attributes.md)<br/>
[Атрибуты класса](class-attributes.md)<br/>
[Атрибуты метода](method-attributes.md)
