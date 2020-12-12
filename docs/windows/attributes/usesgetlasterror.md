---
description: 'Дополнительные сведения о: усесжетластеррор'
title: усесжетластеррор (атрибут COM C++)
ms.date: 10/02/2018
f1_keywords:
- vc-attr.usesgetlasterror
helpviewer_keywords:
- usesgetlasterror attribute
ms.assetid: d149e33d-35a7-46cb-9137-ae6883d86122
ms.openlocfilehash: f43ae005e2f888f4318900cbde58f449011bd15e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97329512"
---
# <a name="usesgetlasterror"></a>usesgetlasterror

Сообщает вызывающему, что при возникновении ошибки при вызове этой функции вызывающий объект может вызвать метод, `GetLastError` чтобы получить код ошибки.

## <a name="syntax"></a>Синтаксис

```cpp
[usesgetlasterror]
```

## <a name="remarks"></a>Remarks

Атрибут **усесжетластеррор** C++ имеет те же функциональные возможности, что и атрибут [усесжетластеррор](/windows/win32/Midl/usesgetlasterror) MIDL.

## <a name="example"></a>Пример

Пример использования **усесжетластеррор** см. в примере [idl_module](idl-module.md) .

## <a name="requirements"></a>Требования

| Контекст атрибута | Значение |
|-|-|
|**Относится к**|атрибут **module**|
|**REPEATABLE**|Нет|
|**Требуемые атрибуты**|Нет|
|**Недопустимые атрибуты**|Нет|

Дополнительные сведения о контекстах атрибутов см. в разделе [Контексты атрибутов](cpp-attributes-com-net.md#contexts).

## <a name="see-also"></a>См. также раздел

[Атрибуты IDL](idl-attributes.md)
