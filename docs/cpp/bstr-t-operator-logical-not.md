---
description: 'Дополнительные сведения о: _bstr_t:: operator!'
title: '_bstr_t:: operator!'
ms.date: 02/02/2021
f1_keywords:
- _bstr_t::operator!
helpviewer_keywords:
- '! operator'
- operator!, bstr
- operator !, bstr
ms.openlocfilehash: 712aeafd26fda6c8291a54a9b897d31fa77ac02e
ms.sourcegitcommit: c20734f18d3d49bb38b1628c68b53b54b3eeeb03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "99522603"
---
# `_bstr_t::operator !`

**Блок, относящийся только к системам Microsoft**

Проверяет, является ли Инкапсулированная `BSTR` строка пустой.

## <a name="syntax"></a>Синтаксис

```cpp
bool operator!( ) const throw( );
```

## <a name="return-value"></a>Возвращаемое значение

Он возвращает **`true`** значение, если инкапсулированный `BSTR` является строкой null, **`false`** Если нет.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[`_bstr_t` см](../cpp/bstr-t-class.md)
