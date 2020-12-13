---
description: 'Дополнительные сведения о: HelpFile'
title: HelpFile (атрибут C++ COM)
ms.date: 10/02/2018
f1_keywords:
- vc-attr.helpfile
helpviewer_keywords:
- helpfile attribute
ms.assetid: d75161c1-1363-4019-ae09-e7e3b8a3971e
ms.openlocfilehash: ff3207c39bc5f83ededb2f7f299cf798b16f0eaa
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97331151"
---
# <a name="helpfile"></a>helpfile

Задает имя файла справки для библиотеки типов.

## <a name="syntax"></a>Синтаксис

```cpp
[ helpfile("filename") ]
```

### <a name="parameters"></a>Параметры

*filename*<br/>
Имя файла, содержащего разделы справки.

## <a name="remarks"></a>Комментарии

Атрибут **HelpFile** C++ имеет те же функциональные возможности, что и атрибут [HelpFile](/windows/win32/Midl/helpfile) MIDL.

## <a name="example"></a>Пример

Пример использования **HelpFile** см. в примере для [модуля](module-cpp.md) .

## <a name="requirements"></a>Требования

| Контекст атрибута | Значение |
|-|-|
|**Относится к**|**интерфейс**, **`typedef`** , **`class`** , метод, **`property`**|
|**REPEATABLE**|Нет|
|**Требуемые атрибуты**|Нет|
|**Недопустимые атрибуты**|Нет|

Дополнительные сведения см. в разделе [Контексты атрибутов](cpp-attributes-com-net.md#contexts).

## <a name="see-also"></a>См. также раздел

[Атрибуты IDL](idl-attributes.md)<br/>
[Атрибуты интерфейса](interface-attributes.md)<br/>
[Атрибуты класса](class-attributes.md)<br/>
[Атрибуты метода](method-attributes.md)<br/>
[Атрибуты typedef, enum, Union и struct](typedef-enum-union-and-struct-attributes.md)<br/>
[helpcontext](helpcontext.md)<br/>
[helpstring](helpstring.md)
