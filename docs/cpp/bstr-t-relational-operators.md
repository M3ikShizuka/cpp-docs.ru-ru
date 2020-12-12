---
description: 'Дополнительные сведения: _bstr_t операторы отношения'
title: Операторы отношения _bstr_t
ms.date: 05/07/2019
f1_keywords:
- _bstr_t::operator>
- _bstr_t::operator==
- _bstr_t::operator>=
- _bstr_t::operator!=
- _bstr_t::operator<
- _bstr_t::operator<=
- _bstr_t::operator!
helpviewer_keywords:
- _bstr_t [C++]
ms.assetid: e153da72-37c3-4d8a-b8eb-730d65da64dd
ms.openlocfilehash: 3d34c83d9547bb9d52e43174cac2acd259717e76
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97308696"
---
# <a name="_bstr_t-relational-operators"></a>Операторы отношения _bstr_t

**Блок, относящийся только к системам Microsoft**

Сравнивает два объекта `_bstr_t`.

## <a name="syntax"></a>Синтаксис

```
bool operator!( ) const throw( );
bool operator==(const _bstr_t& str) const throw( );
bool operator!=(const _bstr_t& str) const throw( );
bool operator<(const _bstr_t& str) const throw( );
bool operator>(const _bstr_t& str) const throw( );
bool operator<=(const _bstr_t& str) const throw( );
bool operator>=(const _bstr_t& str) const throw( );
```

## <a name="remarks"></a>Remarks

Эти операторы производят лексикографическое сравнение двух объектов `_bstr_t` . Операторы возвращают **`true`** , если сравнения содержат, в противном случае возвращает **`false`** .

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Класс _bstr_t](../cpp/bstr-t-class.md)
