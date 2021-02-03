---
description: 'Дополнительные сведения: _bstr_t:: operator ='
title: _bstr_t::operator =
ms.date: 02/02/2021
f1_keywords:
- _bstr_t::operator=
helpviewer_keywords:
- operator = [C++], bstr
- operator= [C++], bstr
ms.openlocfilehash: d021ba013190ddee262b8644e16876401be846dc
ms.sourcegitcommit: c20734f18d3d49bb38b1628c68b53b54b3eeeb03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "99522720"
---
# `_bstr_t::operator =`

**Блок, относящийся только к системам Microsoft**

Присваивает новое значение существующему объекту `_bstr_t`.

## <a name="syntax"></a>Синтаксис

```cpp
_bstr_t& operator=(const _bstr_t& s1) throw ( );
_bstr_t& operator=(const char* s2);
_bstr_t& operator=(const wchar_t* s3);
_bstr_t& operator=(const _variant_t& var);
```

### <a name="parameters"></a>Параметры

*`s1`*\
Объект `_bstr_t`, который требуется присвоить существующему объекту `_bstr_t`.

*`s2`*\
Многобайтовая строка, которую требуется присвоить существующему объекту `_bstr_t`.

*`s3`*\
Строка Юникода, которую требуется присвоить существующему объекту `_bstr_t`.

*`var`*\
Объект `_variant_t`, который требуется присвоить существующему объекту `_bstr_t`.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="example"></a>Пример

См [`_bstr_t::Assign`](../cpp/bstr-t-assign.md) . пример, в котором используется **`operator=`** .

## <a name="see-also"></a>См. также

[`_bstr_t` см](../cpp/bstr-t-class.md)
