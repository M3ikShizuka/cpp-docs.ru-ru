---
description: 'Дополнительные сведения: _bstr_t:: operator ='
title: _bstr_t::operator =
ms.date: 11/04/2016
f1_keywords:
- _bstr_t::operator=
helpviewer_keywords:
- operator = [C++], bstr
- operator= [C++], bstr
ms.assetid: fb31bb1b-ce29-4388-b5fd-8dac830cf18a
ms.openlocfilehash: 78447048a45567df603acf3af0bc51cefbdb187d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97308787"
---
# <a name="_bstr_toperator-"></a>_bstr_t::operator =

**Блок, относящийся только к системам Microsoft**

Присваивает новое значение существующему объекту `_bstr_t`.

## <a name="syntax"></a>Синтаксис

```
_bstr_t& operator=(const _bstr_t& s1) throw ( );
_bstr_t& operator=(const char* s2);
_bstr_t& operator=(const wchar_t* s3);
_bstr_t& operator=(const _variant_t& var);
```

#### <a name="parameters"></a>Параметры

*s1*<br/>
Объект `_bstr_t`, который требуется присвоить существующему объекту `_bstr_t`.

*S2*<br/>
Многобайтовая строка, которую требуется присвоить существующему объекту `_bstr_t`.

*S3*<br/>
Строка Юникода, которую требуется присвоить существующему объекту `_bstr_t`.

*var*<br/>
Объект `_variant_t`, который требуется присвоить существующему объекту `_bstr_t`.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="example"></a>Пример

Пример использования **оператора =** см. в разделе [_Bstr_t:: Assign](../cpp/bstr-t-assign.md) .

## <a name="see-also"></a>См. также раздел

[Класс _bstr_t](../cpp/bstr-t-class.md)
