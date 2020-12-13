---
description: 'Дополнительные сведения о: CW2WEX Class'
title: Класс CW2WEX
ms.date: 11/04/2016
f1_keywords:
- CW2WEX
- ATLCONV/ATL::CW2WEX
- ATLCONV/ATL::CW2WEX::CW2WEX
- ATLCONV/ATL::CW2WEX::m_psz
- ATLCONV/ATL::CW2WEX::m_szBuffer
helpviewer_keywords:
- CW2WEX class
ms.assetid: 46262e56-e0d2-41fe-855b-0b67ecc8fcd7
ms.openlocfilehash: 87dbcefe37a54270b021ee1446ba5ccba2ef8313
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97140248"
---
# <a name="cw2wex-class"></a>Класс CW2WEX

Этот класс используется макросами преобразования строк CW2TEX и CT2WEX, а также typedef CW2W.

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```
template <int t_nBufferLength = 128>
class CW2WEX
```

#### <a name="parameters"></a>Параметры

*t_nBufferLength*<br/>
Размер буфера, используемого в процессе перевода. Длина по умолчанию составляет 128 байт.

## <a name="members"></a>Элементы

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CW2WEX::CW2WEX](#cw2wex)|Конструктор.|
|[CW2WEX:: ~ CW2WEX](#dtor)|Деструктор|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[CW2WEX:: operator LPWSTR](#operator_lpwstr)|Оператор преобразования.|

### <a name="public-data-members"></a>Открытые члены данных

|Имя|Описание|
|----------|-----------------|
|[CW2WEX:: m_psz](#m_psz)|Элемент данных, в котором хранится исходная строка.|
|[CW2WEX:: m_szBuffer](#m_szbuffer)|Статический буфер, используемый для хранения преобразованной строки.|

## <a name="remarks"></a>Комментарии

Если не требуется дополнительных функций, используйте в коде CW2TEX, CT2WEX или CW2W.

Этот класс содержит статический буфер фиксированного размера, который используется для хранения результата преобразования. Если результат слишком велик для использования в статическом буфере, класс выделяет память с помощью функции **malloc**, освобождая память, когда объект выходит из области. Это гарантирует, что, в отличие от макросов преобразования текста, доступных в предыдущих версиях ATL, этот класс можно использовать в циклах, и он не будет переполнен стек.

Если класс пытается выделить память в куче и завершается ошибкой, он вызывается `AtlThrow` с аргументом E_OUTOFMEMORY.

По умолчанию классы и макросы преобразования ATL используют для преобразования кодовую страницу ANSI текущего потока.

Следующие макросы основаны на этом классе:

- CW2TEX

- CT2WEX

Следующий typedef основан на этом классе:

- CW2W

Обсуждение этих макросов преобразования текста см. в разделе [ATL и макросы преобразования строк MFC](string-conversion-macros.md).

## <a name="example"></a>Пример

Пример использования этих макросов преобразования строк см. в разделе [ATL и макросы преобразования строк MFC](string-conversion-macros.md) .

## <a name="requirements"></a>Требования

**Заголовок:** атлконв. h

## <a name="cw2wexcw2wex"></a><a name="cw2wex"></a> CW2WEX::CW2WEX

Конструктор.

```
CW2WEX(LPCWSTR psz, UINT nCodePage) throw(...);
CW2WEX( LPCWSTR  psz) throw(...);
```

### <a name="parameters"></a>Параметры

*псз*<br/>
Текстовая строка для преобразования.

*нкодепаже*<br/>
Кодовая страница. Не используется в этом классе.

### <a name="remarks"></a>Комментарии

Создает буфер, необходимый для перевода.

## <a name="cw2wexcw2wex"></a><a name="dtor"></a> CW2WEX:: ~ CW2WEX

Деструктор.

```
~CW2WEX() throw();
```

### <a name="remarks"></a>Комментарии

Освобождает выделенный буфер.

## <a name="cw2wexm_psz"></a><a name="m_psz"></a> CW2WEX:: m_psz

Элемент данных, в котором хранится исходная строка.

```
LPWSTR m_psz;
```

## <a name="cw2wexm_szbuffer"></a><a name="m_szbuffer"></a> CW2WEX:: m_szBuffer

Статический буфер, используемый для хранения преобразованной строки.

```
wchar_t m_szBuffer[t_nBufferLength];
```

## <a name="cw2wexoperator-lpwstr"></a><a name="operator_lpwstr"></a> CW2WEX:: operator LPWSTR

Оператор CAST.

```
operator LPWSTR() const throw();
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает текстовую строку типа LPWSTR.

## <a name="see-also"></a>См. также раздел

[Класс CA2AEX](../../atl/reference/ca2aex-class.md)<br/>
[Класс CA2CAEX](../../atl/reference/ca2caex-class.md)<br/>
[Класс CA2WEX](../../atl/reference/ca2wex-class.md)<br/>
[Класс CW2AEX](../../atl/reference/cw2aex-class.md)<br/>
[Класс CW2CWEX](../../atl/reference/cw2cwex-class.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
