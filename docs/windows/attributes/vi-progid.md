---
description: 'Дополнительные сведения: vi_progid'
title: vi_progid (атрибут COM C++)
ms.date: 10/02/2018
f1_keywords:
- vc-attr.vi_progid
helpviewer_keywords:
- vi_progid attribute
ms.assetid: a52449be-b93e-4111-b883-44bb8da53261
ms.openlocfilehash: 766ebcee636b3fb0bcdb1aeabd53ee0e977ca790
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97327191"
---
# <a name="vi_progid"></a>vi_progid

Указывает независимую от версии форму ProgID.

## <a name="syntax"></a>Синтаксис

```cpp
[ vi_progid(name) ];
```

### <a name="parameters"></a>Параметры

*name*<br/>
Идентификатор ProgID, не зависящий от версии, представляющий объект.

Идентификаторы ProgID представляют собой удобочитаемую для человека версию идентификатора класса (CLSID), используемую для идентификации объектов COM/ActiveX.

## <a name="remarks"></a>Комментарии

Атрибут **vi_progid** C++ позволяет указать независимый от версии идентификатор ProgID для COM-объекта. Идентификатор ProgID имеет форму *name1. имя2. Version*. Идентификатор ProgID, не зависящий от версии, не имеет *версии*. В можно указать `progid` и атрибут, и **vi_progid** `coclass` . Если не указать **vi_progid**, идентификатор ProgID, не зависящий от версии, является значением, заданным в атрибуте [ProgID](progid.md) .

**vi_progid** подразумевает `coclass` атрибут, то есть если указать **vi_progid**, то это то же самое, что `coclass` и атрибуты и **vi_progid** .

Атрибут **vi_progid** вызывает автоматическую регистрацию класса с указанным именем. Созданный IDL-файл не будет отображать значение ProgID.

В проектах ATL, если атрибут [coclass](coclass.md) также имеется, указанный идентификатор ProgID используется `GetVersionIndependentProgID` функцией (которая вставляется `coclass` атрибутом).

## <a name="example"></a>Пример

Пример использования **vi_progid** см. в примере [компонентного класса](coclass.md) .

## <a name="requirements"></a>Требования

| Контекст атрибута | Значение |
|-|-|
|**Относится к**|**`class`**, **`struct`**|
|**REPEATABLE**|Нет|
|**Требуемые атрибуты**|Нет|
|**Недопустимые атрибуты**|Нет|

Дополнительные сведения о контекстах атрибутов см. в разделе [Контексты атрибутов](cpp-attributes-com-net.md#contexts).

## <a name="see-also"></a>См. также раздел

[Атрибуты IDL](idl-attributes.md)<br/>
[Атрибуты typedef, enum, Union и struct](typedef-enum-union-and-struct-attributes.md)<br/>
[Атрибуты класса](class-attributes.md)<br/>
[Ключ ProgID](/windows/win32/com/-progid--key)
