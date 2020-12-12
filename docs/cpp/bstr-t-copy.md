---
description: 'Дополнительные сведения о: _bstr_t:: Copy'
title: _bstr_t::copy
ms.date: 11/04/2016
f1_keywords:
- _bstr_t::copy
helpviewer_keywords:
- Copy method [C++]
- BSTR object [C++], copy
ms.assetid: 00ba7311-e82e-4a79-8106-5329fa2f869a
ms.openlocfilehash: 29ca965730dbcc22b4b725661ece68442d39aeba
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97229344"
---
# <a name="_bstr_tcopy"></a>_bstr_t::copy

**Блок, относящийся только к системам Microsoft**

Создает копию инкапсулированного объекта `BSTR`.

## <a name="syntax"></a>Синтаксис

```
BSTR copy( bool fCopy = true ) const;
```

#### <a name="parameters"></a>Параметры

*фкопи*<br/>
Если значение **`true`** , **Copy** возвращает копию вложенного объекта `BSTR` , в противном случае **Copy** возвращает фактическую BSTR.

## <a name="remarks"></a>Комментарии

Возвращает копию инкапсулированного объекта `BSTR`, для которого выделена память.

## <a name="example"></a>Пример

```cpp
STDMETHODIMP CAlertMsg::get_ConnectionStr(BSTR *pVal){ //  m_bsConStr is _bstr_t
   *pVal = m_bsConStr.copy();
}
```

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Класс _bstr_t](../cpp/bstr-t-class.md)
