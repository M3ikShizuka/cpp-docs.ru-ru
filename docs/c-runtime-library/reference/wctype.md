---
description: 'Дополнительные сведения о: wctype'
title: wctype
ms.date: 11/04/2016
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
api_type:
- DLLExport
topic_type:
- apiref
f1_keywords:
- wctype
helpviewer_keywords:
- wctype function
- wide characters
ms.assetid: 14aded12-4087-4123-bc48-db4e10999223
ms.openlocfilehash: 0791d4f048dfa5d6804db14d577b1370ffbf8754
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97254200"
---
# <a name="wctype"></a>wctype

Определяет правило классификации кодов расширенных символов.

## <a name="syntax"></a>Синтаксис

```C
wctype_t wctype(
   const char * property
);
```

### <a name="parameters"></a>Параметры

*property*<br/>
Строка свойства.

## <a name="return-value"></a>Возвращаемое значение

Если категория **LC_CTYPE** текущего языкового стандарта не определяет правило классификации, имя которого соответствует *свойству* строки свойства, функция возвращает ноль. В противном случае возвращается ненулевое значение, подходящее для использования в качестве второго аргумента последующего вызова [towctrans](towctrans.md).

## <a name="remarks"></a>Комментарии

Функция определяет правило классификации кодов расширенных символов. Следующие пары вызовов имеют аналогичное поведение во всех языковых стандартах (но реализация позволяет определить дополнительные правила классификации даже в языковом стандарте "C").

|Функция|Эквивалентно|
|--------------|-------------|
|исвалнум (c)|iswctype (c, wctype ("алнум"))|
|исвалфа (c)|iswctype (c, wctype ("Альфа"))|
|исвкнтрл (c)|iswctype (c, wctype ("Вкладка"))|
|исвдигит (c)|iswctype (c, wctype ("digit"))|
|исвграф (c)|iswctype (c, wctype ("Graph"))|
|iswlower (c)|iswctype (c, wctype ("ниже"))|
|исвпринт (c)|iswctype (c, wctype ("Печать"))|
|исвпункт (c)|iswctype (c, wctype ("punct"))|
|исвспаце (c)|iswctype (c, wctype ("пробел"))|
|iswupper (c)|iswctype (c, wctype ("Upper"))|
|исвксдигит (c)|iswctype (c, wctype ("ксдигит"))|

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|**wctype**|\<wctype.h>|

Дополнительные сведения о совместимости см. в статье [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="see-also"></a>См. также раздел

[Преобразование данных](../../c-runtime-library/data-conversion.md)<br/>
[setlocale, _wsetlocale](setlocale-wsetlocale.md)<br/>
