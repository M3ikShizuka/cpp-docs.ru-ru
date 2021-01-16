---
description: 'Дополнительные сведения о: wctype'
title: wctype
ms.date: 1/14/2021
api_name:
- wctype
api_location:
- msvcrt.dll
- msvcr80.dll
- msvcr90.dll
- msvcr100.dll
- msvcr100_clr0400.dll
- msvcr110.dll
- msvcr110_clr0400.dll
- msvcr120.dll
- msvcr120_clr0400.dll
- ucrtbase.dll
- api-ms-win-crt-string-l1-1-0.dll
api_type:
- DLLExport
topic_type:
- apiref
f1_keywords:
- wctype
helpviewer_keywords:
- wctype function
- wide characters
ms.openlocfilehash: d0afd2bd163af967b11d0df58c84b62521ca6c2a
ms.sourcegitcommit: 1cd8f8a75fd036ffa57bc70f3ca869042d8019d4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "98242933"
---
# `wctype`

Определяет правило классификации кодов расширенных символов.

## <a name="syntax"></a>Синтаксис

```C
wctype_t wctype(
   const char * property
);
```

### <a name="parameters"></a>Параметры

*`property`*\
Строка свойства.

## <a name="return-value"></a>Возвращаемое значение

Если **`LC_CTYPE`** Категория текущего языкового стандарта не определяет правило классификации, имя которого совпадает со строкой свойства *`property`* , функция возвращает ноль. В противном случае возвращается ненулевое значение, подходящее для использования в качестве второго аргумента для последующего вызова [`towctrans`](towctrans.md) .

## <a name="remarks"></a>Комментарии

Функция определяет правило классификации кодов расширенных символов. Следующие пары вызовов имеют аналогичное поведение во всех языковых стандартах (но реализация позволяет определить дополнительные правила классификации даже в языковом стандарте "C").

|Функция|Эквивалентно|
|--------------|-------------|
|`iswalnum(c)`|`iswctype(c, wctype( "alnum" ))`|
|`iswalpha(c)`|`iswctype(c, wctype( "alpha" ))`|
|`iswcntrl(c)`|`iswctype(c, wctype( "cntrl" ))`|
|`iswdigit(c)`|`iswctype(c, wctype( "digit" ))`|
|`iswgraph(c)`|`iswctype(c, wctype( "graph" ))`|
|`iswlower(c)`|`iswctype(c, wctype( "lower" ))`|
|`iswprint(c)`|`iswctype(c, wctype( "print" ))`|
|`iswpunct(c)`|`iswctype(c, wctype( "punct" ))`|
|`iswspace(c)`|`iswctype(c, wctype( "space" ))`|
|`iswupper(c)`|`iswctype(c, wctype( "upper" ))`|
|`iswxdigit(c)`|`iswctype(c, wctype( "xdigit" ))`|

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|`wctype`|`<wctype.h>`|

Дополнительные сведения о совместимости см. в разделе [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="see-also"></a>См. также

[Преобразование данных](../../c-runtime-library/data-conversion.md)\
[`setlocale`, `_wsetlocale`](setlocale-wsetlocale.md)
