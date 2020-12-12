---
description: 'Дополнительные сведения: no_injected_text'
title: no_injected_text (атрибут COM C++)
ms.date: 10/02/2018
f1_keywords:
- vc-attr.no_injected_text
helpviewer_keywords:
- no_injected_text attribute
ms.assetid: 5256f808-e41e-4f4a-9ea5-e447919f5696
ms.openlocfilehash: 3d6b4b77055b6706256b25b0b722034e0275ec19
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97327478"
---
# <a name="no_injected_text"></a>no_injected_text

Не позволяет компилятору внедрять код в результате использования атрибута.

## <a name="syntax"></a>Синтаксис

```cpp
[ no_injected_text(boolean) ];
```

### <a name="parameters"></a>Параметры

*boolean*<br/>
(Необязательно) **`true`** Если вы не хотите внедрять код, **`false`** чтобы разрешить внедрение кода. **`true`** значение по умолчанию —.

## <a name="remarks"></a>Комментарии

Наиболее распространенным применением атрибута **no_injected_text** C++ является параметр компилятора [/FX](../../build/reference/fx-merge-injected-code.md) , который вставляет атрибут **no_injected_text** в MRG-файл.

## <a name="requirements"></a>Требования

| Контекст атрибута | Значение |
|-|-|
|**Относится к**|В любом месте|
|**REPEATABLE**|Нет|
|**Требуемые атрибуты**|Нет|
|**Недопустимые атрибуты**|Нет|

Дополнительные сведения о контекстах атрибутов см. в разделе [Контексты атрибутов](cpp-attributes-com-net.md#contexts).

## <a name="see-also"></a>См. также раздел

[Атрибуты компилятора](compiler-attributes.md)
