---
description: 'Дополнительные сведения: _bstr_t:: wchar_t *, _bstr_t:: char*'
title: _bstr_t::wchar_t *, _bstr_t::char*
ms.date: 02/02/2021
f1_keywords:
- _bstr_t::wchar_t*
- _bstr_t::char*
helpviewer_keywords:
- operator wchar_t* [C++]
- operator char* [C++]
ms.openlocfilehash: b2e98ea4b62d4a2e346b552d31d66d23f301817c
ms.sourcegitcommit: c20734f18d3d49bb38b1628c68b53b54b3eeeb03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "99522551"
---
# <a name="_bstr_twchar_t-_bstr_tchar"></a>`_bstr_t::wchar_t*`, `_bstr_t::char*`

**Блок, относящийся только к системам Microsoft**

Возвращает `BSTR` символы в виде узких или расширенных массивов символов.

## <a name="syntax"></a>Синтаксис

```cpp
operator const wchar_t*( ) const throw( );
operator wchar_t*( ) const throw( );
operator const char*( ) const;
operator char*( ) const;
```

## <a name="remarks"></a>Примечания

Эти операторы можно использовать для извлечения символьных данных, инкапсулированных `BSTR` объектом. Присвоение возвращенному указателю нового значения не приводит к изменению исходных `BSTR` данных.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[`_bstr_t` см](../cpp/bstr-t-class.md)
