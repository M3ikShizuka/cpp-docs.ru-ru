---
description: 'Дополнительные сведения: запись'
title: Entry (атрибут COM C++)
ms.date: 10/02/2018
f1_keywords:
- vc-attr.entry
helpviewer_keywords:
- entry attribute
ms.assetid: ba4843e3-d7ad-4b86-9a15-0b4192f0f698
ms.openlocfilehash: fbceea4c23d730ceba780ce68398a9d78fa9c33b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97259231"
---
# <a name="entry"></a>entry

Указывает экспортированную функцию или константу в модуле, определяя точку входа в библиотеке DLL.

## <a name="syntax"></a>Синтаксис

```cpp
[ entry(id) ]
```

### <a name="parameters"></a>Параметры

*id*<br/>
Идентификатор точки входа.

## <a name="remarks"></a>Комментарии

Атрибут **entry** C++ имеет те же функциональные возможности, что и атрибут MIDL [элемента](/windows/win32/Midl/entry) .

## <a name="example"></a>Пример

Пример использования **записи** см. в примере для [idl_module](idl-module.md) .

## <a name="requirements"></a>Требования

| Контекст атрибута | Значение |
|-|-|
|**Относится к**|Атрибут `idl_module`|
|**REPEATABLE**|Нет|
|**Требуемые атрибуты**|Нет|
|**Недопустимые атрибуты**|Нет|

Дополнительные сведения см. в разделе [Контексты атрибутов](cpp-attributes-com-net.md#contexts).

## <a name="see-also"></a>См. также раздел

[Атрибуты IDL](idl-attributes.md)
