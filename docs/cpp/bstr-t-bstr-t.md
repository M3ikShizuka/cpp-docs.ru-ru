---
description: 'Дополнительные сведения: _bstr_t:: _bstr_t'
title: _bstr_t::_bstr_t
ms.date: 02/02/2021
f1_keywords:
- _bstr_t::_bstr_t
helpviewer_keywords:
- BSTR object
- _bstr_t method [C++]
- _bstr_t class
ms.openlocfilehash: 0e6913a45b1c4d542e495bc59bc5871f533a1573
ms.sourcegitcommit: c20734f18d3d49bb38b1628c68b53b54b3eeeb03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "99522915"
---
# `_bstr_t::_bstr_t`

**Блок, относящийся только к системам Microsoft**

Формирует объект `_bstr_t`.

## <a name="syntax"></a>Синтаксис

```cpp
_bstr_t( ) throw( );
_bstr_t(
   const _bstr_t& s1
) throw( );
_bstr_t(
   const char* s2
);
_bstr_t(
   const wchar_t* s3
);
_bstr_t(
   const _variant_t& var
);
_bstr_t(
   BSTR bstr,
   bool fCopy
);
```

### <a name="parameters"></a>Параметры

*`s1`*\
Копируемый объект `_bstr_t`.

*`s2`*\
Многобайтовая строка.

*`s3`*\
Строка Юникода.

*`var`*\
Объект [_variant_t](../cpp/variant-t-class.md) .

*`bstr`*\
Существующий объект `BSTR`.

*`fCopy`*\
Если **`false`** значение *`bstr`* равно, аргумент прикрепляется к новому объекту без создания копии путем вызова метода `SysAllocString` .

## <a name="remarks"></a>Примечания

`_bstr_t`Класс предоставляет несколько конструкторов:

`_bstr_t( )`\
Конструирует объект по умолчанию `_bstr_t` , инкапсулирующий `BSTR` объект null.

`_bstr_t( _bstr_t& s1 )`\
Создает объект `_bstr_t` как копию другого объекта. Этот конструктор создает *неполную* копию, которая увеличивает счетчик ссылок инкапсулированного `BSTR` объекта, а не создает новый.

`_bstr_t( char* s2 )`\
Создает новый объект `_bstr_t`, вызывая функцию `SysAllocString` для создания нового объекта `BSTR`, а затем инкапсулирует его. Этот конструктор конструктор сначала преобразует многобайтовую строку в строку Юникода.

`_bstr_t( wchar_t* s3 )`\
Создает новый объект `_bstr_t`, вызывая функцию `SysAllocString` для создания нового объекта `BSTR`, а затем инкапсулирует его.

`_bstr_t( _variant_t& var )`\
Конструирует `_bstr_t` объект из `_variant_t` объекта, сначала получая `BSTR` объект из инкапсулированного `VARIANT` объекта.

`_bstr_t( BSTR bstr, bool fCopy )`\
Создает объект `_bstr_t` из существующего объекта `BSTR` (а не из строки `wchar_t*`). Если *`fCopy`* имеет значение **`false`** , предоставленный `BSTR` объект присоединяется к новому объекту без создания новой копии с помощью `SysAllocString` . Этот конструктор используется функциями-оболочками в заголовках библиотек типов для инкапсуляции и получения владения объектом `BSTR` , возвращаемым методом интерфейса.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[`_bstr_t` см](../cpp/bstr-t-class.md)\
[`_variant_t` см](../cpp/variant-t-class.md)
