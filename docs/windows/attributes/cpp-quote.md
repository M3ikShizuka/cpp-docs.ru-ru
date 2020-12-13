---
description: 'Дополнительные сведения: cpp_quote'
title: cpp_quote (атрибут COM C++)
ms.date: 10/02/2018
f1_keywords:
- vc-attr.cpp_quote
helpviewer_keywords:
- cpp_quote attribute
ms.assetid: f75327ff-42bd-498b-9177-7ffa25427e1f
ms.openlocfilehash: fe8424fd16cb75e320f8c1a1f8e3e444cf2185ea
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97333174"
---
# <a name="cpp_quote"></a>cpp_quote

Порождает указанную строку без кавычек в созданный IDL-файл.

## <a name="syntax"></a>Синтаксис

```cpp
[ cpp_quote("statement") ];
```

### <a name="parameters"></a>Параметры

*инструкция*<br/>
Инструкция C.

## <a name="remarks"></a>Комментарии

Атрибут **cpp_quote** C++ полезен, если вы хотите поместить директиву препроцессора в IDL-файл.

Можно также использовать **cpp_quote** и создать h файл в составе компиляции MIDL. Например, если имеется файл заголовка C++, который использует атрибуты IDL C++, но не может использовать этот файл для некоторой задачи, можно скомпилировать его, чтобы создать h-файл, созданный с помощью MIDL, который вы должны иметь возможность использовать.

Атрибут **cpp_quote** имеет те же функциональные возможности, что и атрибут [cpp_quote](/windows/win32/Midl/cpp-quote) MIDL.

## <a name="example"></a>Пример

См. пример для [Dual](dual.md) в качестве примера использования **cpp_quote**.

## <a name="requirements"></a>Требования

| Контекст атрибута | Значение |
|-|-|
|**Относится к**|В любом месте|
|**REPEATABLE**|Нет|
|**Требуемые атрибуты**|Нет|
|**Недопустимые атрибуты**|Нет|

Дополнительные сведения о контекстах атрибутов см. в разделе [Контексты атрибутов](cpp-attributes-com-net.md#contexts).

## <a name="see-also"></a>См. также раздел

[Атрибуты IDL](idl-attributes.md)<br/>
[Изолированные атрибуты](stand-alone-attributes.md)
