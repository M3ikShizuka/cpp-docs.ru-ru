---
description: 'Дополнительные сведения о: CA2CAEX Class'
title: Класс CA2CAEX
ms.date: 11/04/2016
f1_keywords:
- CA2CAEX
- ATLCONV/ATL::CA2CAEX
- ATLCONV/ATL::CA2CAEX::CA2CAEX
- ATLCONV/ATL::CA2CAEX::m_psz
helpviewer_keywords:
- CA2CAEX class
ms.assetid: 388e7c1d-a144-474c-a182-b15f69a74bd8
ms.openlocfilehash: 89709280e94e07c549d179dc9a9863bd4bf2cbaa
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97158599"
---
# <a name="ca2caex-class"></a>Класс CA2CAEX

Этот класс используется макросами преобразования строк CA2CTEX и CT2CAEX, а также typedef CA2CA.

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```cpp
template<int t_nBufferLength = 128>
class CA2CAEX
```

### <a name="parameters"></a>Параметры

*t_nBufferLength*<br/>
Размер буфера, используемого в процессе перевода. Длина по умолчанию составляет 128 байт.

## <a name="members"></a>Элементы

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CA2CAEX::CA2CAEX](#ca2caex)|Конструктор.|
|[CA2CAEX:: ~ CA2CAEX](#dtor)|Деструктор|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[CA2CAEX:: operator LPCSTR](#operator_lpcstr)|Оператор преобразования.|

### <a name="public-data-members"></a>Открытые члены данных

|Имя|Описание|
|----------|-----------------|
|[CA2CAEX:: m_psz](#m_psz)|Элемент данных, в котором хранится исходная строка.|

## <a name="remarks"></a>Комментарии

Если не требуется дополнительных функций, используйте CA2CTEX, CT2CAEX или CA2CA в своем коде.

Этот класс можно использовать в циклах и не будет переполнен стеком. По умолчанию классы и макросы преобразования ATL используют для преобразования кодовую страницу ANSI текущего потока.

Следующие макросы основаны на этом классе:

- CA2CTEX

- CT2CAEX

Следующий typedef основан на этом классе:

- CA2CA

Обсуждение этих макросов преобразования текста см. в разделе [ATL и макросы преобразования строк MFC](string-conversion-macros.md).

## <a name="example"></a>Пример

Пример использования этих макросов преобразования строк см. в разделе [ATL и макросы преобразования строк MFC](string-conversion-macros.md) .

## <a name="requirements"></a>Требования

**Заголовок:** атлконв. h

## <a name="ca2caexca2caex"></a><a name="ca2caex"></a> CA2CAEX::CA2CAEX

Конструктор.

```cpp
CA2CAEX(LPCSTR psz, UINT nCodePage) throw(...);
CA2CAEX(LPCSTR psz) throw(...);
```

### <a name="parameters"></a>Параметры

*псз*<br/>
Текстовая строка для преобразования.

*нкодепаже*<br/>
Не используется в этом классе.

### <a name="remarks"></a>Комментарии

Создает буфер, необходимый для перевода.

## <a name="ca2caexca2caex"></a><a name="dtor"></a> CA2CAEX:: ~ CA2CAEX

Деструктор

```cpp
~CA2CAEX() throw();
```

### <a name="remarks"></a>Комментарии

Освобождает выделенный буфер.

## <a name="ca2caexm_psz"></a><a name="m_psz"></a> CA2CAEX:: m_psz

Элемент данных, в котором хранится исходная строка.

```cpp
LPCSTR m_psz;
```

## <a name="ca2caexoperator-lpcstr"></a><a name="operator_lpcstr"></a> CA2CAEX:: operator LPCSTR

Оператор преобразования.

```cpp
operator LPCSTR() const throw();
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает текстовую строку как тип LPCSTR.

## <a name="see-also"></a>См. также раздел

[Класс CA2AEX](../../atl/reference/ca2aex-class.md)<br/>
[Класс CA2WEX](../../atl/reference/ca2wex-class.md)<br/>
[Класс CW2AEX](../../atl/reference/cw2aex-class.md)<br/>
[Класс CW2CWEX](../../atl/reference/cw2cwex-class.md)<br/>
[Класс CW2WEX](../../atl/reference/cw2wex-class.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
