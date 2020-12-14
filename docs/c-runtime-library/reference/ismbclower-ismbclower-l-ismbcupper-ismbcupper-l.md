---
description: 'Дополнительные сведения: _ismbclower, _ismbclower_l, _ismbcupper, _ismbcupper_l'
title: _ismbclower, _ismbclower_l, _ismbcupper, _ismbcupper_l
ms.date: 4/2/2020
api_name:
- _ismbclower
- _ismbclower_l
- _ismbcupper_l
- _ismbcupper
- _o__ismbclower
- _o__ismbclower_l
- _o__ismbcupper
- _o__ismbcupper_l
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
- api-ms-win-crt-multibyte-l1-1-0.dll
- api-ms-win-crt-private-l1-1-0.dll
api_type:
- DLLExport
topic_type:
- apiref
f1_keywords:
- _ismbcupper
- _ismbclower
helpviewer_keywords:
- _ismbcupper function
- ismbclower function
- _ismbclower_l function
- ismbcupper_l function
- _ismbclower function
- ismbcupper function
- ismbclower_l function
- _ismbcupper_l function
ms.assetid: 17d89587-65bc-477c-ba8f-a84e63cf59e7
ms.openlocfilehash: c4afed88aff750be44602270b0bc7c2e3fa77073
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97279667"
---
# <a name="_ismbclower-_ismbclower_l-_ismbcupper-_ismbcupper_l"></a>_ismbclower, _ismbclower_l, _ismbcupper, _ismbcupper_l

Проверяет, имеет ли многобайтовый символ нижний или верхний регистр.

> [!IMPORTANT]
> Этот API нельзя использовать в приложениях, выполняемых в среде выполнения Windows. Дополнительные сведения: [Функции CRT, которые не поддерживаются в приложениях универсальной платформы Windows](../../cppcx/crt-functions-not-supported-in-universal-windows-platform-apps.md).

## <a name="syntax"></a>Синтаксис

```C
int _ismbclower(
   unsigned int c
);
int _ismbclower_l(
   unsigned int c,
   _locale_t locale
);
int _ismbcupper(
   unsigned int c
);
int _ismbcupper_l(
   unsigned int c,
   _locale_t locale
);
```

### <a name="parameters"></a>Параметры

*c*<br/>
Символ, который требуется проверить.

*locale*<br/>
Используемый языковой стандарт.

## <a name="return-value"></a>Возвращаемое значение

Каждая из этих процедур возвращает ненулевое значение, если символ удовлетворяет условию теста, или 0, если не удовлетворяет. Если *c*<= 255 и имеется соответствующая **_ismbbая** под (например, **_ismbcalnum** соответствует **_ismbbalnum**), результатом является возвращаемое значение соответствующей подпрограммы **_ismbb** .

## <a name="remarks"></a>Комментарии

Каждая из этих функций проверяет определенный многобайтовый символ на соответствие заданному условию.

Версии этих функций с суффиксом **_l** идентичны за исключением того, что они используют переданный языковой стандарт вместо текущего языкового стандарта для поведения, зависящего от языкового стандарта. Для получения дополнительной информации см. [Locale](../../c-runtime-library/locale.md).

|Подпрограмма|Условие теста|Пример кодовой страницы 932|
|-------------|--------------------|---------------------------|
|**_ismbclower**|Строчные буквы|Возвращает ненулевое значение только в том случае, если *c* является однобайтовым представлением буквы английского алфавита в кодировке ASCII: 0x61<=*c*<= 0x7A.|
|**_ismbclower_l**|Строчные буквы|Возвращает ненулевое значение только в том случае, если *c* является однобайтовым представлением буквы английского алфавита в кодировке ASCII: 0x61<=*c*<= 0x7A.|
|**_ismbcupper**|Прописные буквы|Возвращает ненулевое значение только в том случае, если *c* является однобайтовым представлением буквы английского алфавита в кодировке ASCII: 0x41 влево<=*c*<= 0x5A.|
|**_ismbcupper_l**|Прописные буквы|Возвращает ненулевое значение только в том случае, если *c* является однобайтовым представлением буквы английского алфавита в кодировке ASCII: 0x41 влево<=*c*<= 0x5A.|

По умолчанию глобальное состояние этой функции ограничивается приложением. Чтобы изменить это, см. раздел [глобальное состояние в CRT](../global-state.md).

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|**_ismbclower**|\<mbstring.h>|
|**_ismbclower_l**|\<mbstring.h>|
|**_ismbcupper**|\<mbstring.h>|
|**_ismbcupper_l**|\<mbstring.h>|

Дополнительные сведения о совместимости см. в разделе [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="see-also"></a>См. также раздел

[Классификация символов](../../c-runtime-library/character-classification.md)<br/>
[подпрограммы _ismbc](../../c-runtime-library/ismbc-routines.md)<br/>
[Локаль](../../c-runtime-library/locale.md)<br/>
[Интерпретация последовательностей Multibyte-Character](../../c-runtime-library/interpretation-of-multibyte-character-sequences.md)<br/>
[является, подпрограммы isw](../../c-runtime-library/is-isw-routines.md)<br/>
[подпрограммы _ismbb](../../c-runtime-library/ismbb-routines.md)<br/>
