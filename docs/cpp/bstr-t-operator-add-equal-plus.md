---
description: 'Дополнительные сведения: _bstr_t:: operator + =, +'
title: _bstr_t::operator +=, +
ms.date: 11/04/2016
f1_keywords:
- _bstr_t::operator+
- _bstr_t::operator+=
helpviewer_keywords:
- += operator [C++], appending strings
- + operator [C++], _bstr_t objects
ms.assetid: d28316ce-c2c8-4a38-bdb3-44fa4e582c44
ms.openlocfilehash: e3ae71a3a43e189251ac0ddaf77572656a031aaf
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97308813"
---
# <a name="_bstr_toperator--"></a>_bstr_t::operator +=, +

**Блок, относящийся только к системам Microsoft**

Добавляет символы в конец объекта `_bstr_t` или объединяет две строки.

## <a name="syntax"></a>Синтаксис

```
_bstr_t& operator+=( const _bstr_t& s1 );
_bstr_t operator+( const _bstr_t& s1 );
friend _bstr_t operator+( const char* s2, const _bstr_t& s1);
friend _bstr_t operator+( const wchar_t* s3, const _bstr_t& s1);
```

#### <a name="parameters"></a>Параметры

*s1*<br/>
Объект `_bstr_t`.

*S2*<br/>
Многобайтовая строка.

*S3*<br/>
Строка Юникода.

## <a name="remarks"></a>Комментарии

Эти операторы выполняют объединение строк:

- **operator + = (**  *S1*  **)** Добавляет символы в инкапсулированном `BSTR` объекте *S1* в конец инкапсулированного объекта `BSTR` .

- **operator + (**  *S1*  **)** Возвращает новый `_bstr_t` объект, сформированный путем сцепления этого объекта `BSTR` с объектом *S1*.

- **operator + (***S2* **&#124;** *S1***)** Возвращает новый объект `_bstr_t` , сформированный путем сцепления многобайтовой строки *S2*, преобразованной в Юникод, с `BSTR` инкапсулированным в *S1*.        

- **оператор + (***S3* **,***S1***)** Возвращает новый объект `_bstr_t` , сформированный путем сцепления строки в Юникоде  с `BSTR` инкапсулированным в *S1*.      

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Класс _bstr_t](../cpp/bstr-t-class.md)
