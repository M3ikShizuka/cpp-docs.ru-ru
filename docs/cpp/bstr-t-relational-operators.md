---
description: 'Дополнительные сведения: _bstr_t операторы отношения'
title: Операторы отношения _bstr_t
ms.date: 02/02/2021
f1_keywords:
- _bstr_t::operator>
- _bstr_t::operator==
- _bstr_t::operator>=
- _bstr_t::operator!=
- _bstr_t::operator<
- _bstr_t::operator<=
helpviewer_keywords:
- _bstr_t relational operators[C++]
ms.openlocfilehash: eef66f8165fc1dfbb29730507ee8d3b996800b7b
ms.sourcegitcommit: c20734f18d3d49bb38b1628c68b53b54b3eeeb03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "99522590"
---
# <a name="_bstr_t-relational-operators"></a>`_bstr_t` Операторы отношения

**Блок, относящийся только к системам Microsoft**

Сравнивает два объекта `_bstr_t`.

## <a name="syntax"></a>Синтаксис

```cpp
bool operator==(const _bstr_t& str) const throw( );
bool operator!=(const _bstr_t& str) const throw( );
bool operator<(const _bstr_t& str) const throw( );
bool operator>(const _bstr_t& str) const throw( );
bool operator<=(const _bstr_t& str) const throw( );
bool operator>=(const _bstr_t& str) const throw( );
```

## <a name="remarks"></a>Примечания

Эти операторы производят лексикографическое сравнение двух объектов `_bstr_t` . Операторы возвращают **`true`** , если сравнения содержат, в противном случае возвращает **`false`** .

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[`_bstr_t` см](../cpp/bstr-t-class.md)
