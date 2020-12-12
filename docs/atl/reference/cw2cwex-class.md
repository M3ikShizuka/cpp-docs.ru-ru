---
description: 'Дополнительные сведения о: CW2CWEX Class'
title: Класс CW2CWEX
ms.date: 11/04/2016
f1_keywords:
- CW2CWEX
- ATLCONV/ATL::CW2CWEX
- ATLCONV/ATL::CW2CWEX::CW2CWEX
- ATLCONV/ATL::CW2CWEX::m_psz
helpviewer_keywords:
- CW2CWEX class
ms.assetid: d654b22b-05a6-410f-a0ec-9a2cbbb4cca7
ms.openlocfilehash: 769dcedf1a9dc15129b09e3305330de33242562e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97140235"
---
# <a name="cw2cwex-class"></a>Класс CW2CWEX

Этот класс используется макросами преобразования строк CW2CTEX и CT2CWEX, а также typedef CW2W.

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```
template<int t_nBufferLength = 128>
class CW2CWEX
```

#### <a name="parameters"></a>Параметры

*t_nBufferLength*<br/>
Размер буфера, используемого в процессе перевода. Длина по умолчанию составляет 128 байт.

## <a name="members"></a>Элементы

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CW2CWEX::CW2CWEX](#cw2cwex)|Конструктор.|
|[CW2CWEX:: ~ CW2CWEX](#dtor)|Деструктор|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[CW2CWEX:: operator ЛПКВСТР](#operator_lpcwstr)|Оператор преобразования.|

### <a name="public-data-members"></a>Открытые члены данных

|Имя|Описание|
|----------|-----------------|
|[CW2CWEX:: m_psz](#m_psz)|Элемент данных, в котором хранится исходная строка.|

## <a name="remarks"></a>Комментарии

Если не требуется дополнительных функций, используйте в коде CW2CTEX, CT2CWEX или CW2W.

Этот класс можно использовать в циклах и не будет переполнен стеком. По умолчанию классы и макросы преобразования ATL используют для преобразования кодовую страницу ANSI текущего потока.

Следующие макросы основаны на этом классе:

- CW2CTEX

- CT2CWEX

Следующий typedef основан на этом классе:

- CW2W

Обсуждение этих макросов преобразования текста см. в разделе [ATL и макросы преобразования строк MFC](string-conversion-macros.md).

## <a name="example"></a>Пример

Пример использования этих макросов преобразования строк см. в разделе [ATL и макросы преобразования строк MFC](string-conversion-macros.md) .

## <a name="requirements"></a>Требования

**Заголовок:** атлконв. h

## <a name="cw2cwexcw2cwex"></a><a name="cw2cwex"></a> CW2CWEX::CW2CWEX

Конструктор.

```
CW2CWEX(LPCWSTR psz, UINT nCodePage) throw(...);
CW2CWEX(LPCWSTR psz) throw(...);
```

### <a name="parameters"></a>Параметры

*псз*<br/>
Текстовая строка для преобразования.

*нкодепаже*<br/>
Кодовая страница. Не используется в этом классе.

### <a name="remarks"></a>Комментарии

Выделяет буфер, используемый в процессе перевода.

## <a name="cw2cwexcw2cwex"></a><a name="dtor"></a> CW2CWEX:: ~ CW2CWEX

Деструктор

```
~CW2CWEX() throw();
```

### <a name="remarks"></a>Комментарии

Освобождает выделенный буфер.

## <a name="cw2cwexm_psz"></a><a name="m_psz"></a> CW2CWEX:: m_psz

Элемент данных, в котором хранится исходная строка.

```
LPCWSTR m_psz;
```

## <a name="cw2cwexoperator-lpcwstr"></a><a name="operator_lpcwstr"></a> CW2CWEX:: operator ЛПКВСТР

Оператор преобразования.

```
operator LPCWSTR() const throw();
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает текстовую строку как тип ЛПКВСТР.

## <a name="see-also"></a>См. также раздел

[Класс CA2AEX](../../atl/reference/ca2aex-class.md)<br/>
[Класс CA2CAEX](../../atl/reference/ca2caex-class.md)<br/>
[Класс CA2WEX](../../atl/reference/ca2wex-class.md)<br/>
[Класс CW2AEX](../../atl/reference/cw2aex-class.md)<br/>
[Класс CW2WEX](../../atl/reference/cw2wex-class.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
