---
description: 'Дополнительные сведения о: _bstr_t:: Copy'
title: _bstr_t::copy
ms.date: 02/02/2021
f1_keywords:
- _bstr_t::copy
helpviewer_keywords:
- Copy method [C++]
- BSTR object [C++], copy
ms.openlocfilehash: 98726e0c3100851d1496e532310ece2209d71ae0
ms.sourcegitcommit: c20734f18d3d49bb38b1628c68b53b54b3eeeb03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "99522863"
---
# `_bstr_t::copy`

**Блок, относящийся только к системам Microsoft**

Создает копию инкапсулированного объекта `BSTR`.

## <a name="syntax"></a>Синтаксис

```cpp
BSTR copy( bool fCopy = true ) const;
```

### <a name="parameters"></a>Параметры

*`fCopy`*\
Если **`true`** значение **`copy`** равно, функция возвращает копию вложенного объекта `BSTR` , в противном случае **`copy`** возвращает фактическую `BSTR` .

## <a name="remarks"></a>Примечания

Возвращает только что выделенную копию инкапсулированного `BSTR` объекта или самого инкапсулированного объекта в зависимости от параметра.

## <a name="example"></a>Пример

```cpp
STDMETHODIMP CAlertMsg::get_ConnectionStr(BSTR *pVal){ //  m_bsConStr is _bstr_t
   *pVal = m_bsConStr.copy();
}
```

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[`_bstr_t` см](../cpp/bstr-t-class.md)
