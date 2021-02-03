---
description: 'Дополнительные сведения: _bstr_t:: operator + =, _bstr_t:: operator +'
title: '_bstr_t:: operator + =, _bstr_t:: operator +'
ms.date: 02/02/2021
f1_keywords:
- _bstr_t::operator+
- _bstr_t::operator+=
helpviewer_keywords:
- += operator [C++], appending strings
- + operator [C++], _bstr_t objects
ms.openlocfilehash: 44a525891ee072ea797026bd022ecae7b62fd6d1
ms.sourcegitcommit: c20734f18d3d49bb38b1628c68b53b54b3eeeb03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "99522525"
---
# <a name="_bstr_toperator--_bstr_toperator-"></a>`_bstr_t::operator +=`, `_bstr_t::operator +`

**Блок, относящийся только к системам Microsoft**

Добавляет символы в конец `_bstr_t` объекта или объединяет две строки.

## <a name="syntax"></a>Синтаксис

```cpp
_bstr_t& operator+=( const _bstr_t& s1 );
_bstr_t operator+( const _bstr_t& s1 );
friend _bstr_t operator+( const char* s2, const _bstr_t& s1);
friend _bstr_t operator+( const wchar_t* s3, const _bstr_t& s1);
```

### <a name="parameters"></a>Параметры

*`s1`*\
Объект `_bstr_t`.

*`s2`*\
Многобайтовая строка.

*`s3`*\
Строка Юникода.

## <a name="remarks"></a>Примечания

Эти операторы выполняют объединение строк:

- `operator+=( s1 )` Добавляет символы в инкапсулированный в `BSTR` *`s1`* конец инкапсулированного объекта `BSTR` .

- `operator+( s1 )` Возвращает новый `_bstr_t` объект, сформированный путем сцепления этого объекта с `BSTR` и его в *`s1`* .

- `operator+( s2, s1 )` Возвращает новый объект `_bstr_t` , сформированный путем сцепления многобайтовой строки *`s2`* , преобразованной в Юникод, и `BSTR` инкапсулированного в *`s1`* .

- `operator+( s3, s1 )` Возвращает новый объект `_bstr_t` , сформированный путем сцепления строки в Юникоде *`s3`* и `BSTR` инкапсулированной в *`s1`* .

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[`_bstr_t` см](../cpp/bstr-t-class.md)
