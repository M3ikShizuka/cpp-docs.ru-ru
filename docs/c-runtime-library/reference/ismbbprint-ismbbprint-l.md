---
description: 'Дополнительные сведения: _ismbbprint, _ismbbprint_l'
title: _ismbbprint, _ismbbprint_l
ms.date: 4/2/2020
api_name:
- _ismbbprint_l
- _ismbbprint
- _o__ismbbprint
- _o__ismbbprint_l
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
- _ismbbprint_l
- _ismbbprint
- ismbbprint
- ismbbprint_l
helpviewer_keywords:
- ismbbprint_l function
- ismbbprint function
- _ismbbprint function
- _ismbbprint_l function
ms.assetid: d08a061c-18a8-48f2-a75d-bff4870aec9d
ms.openlocfilehash: e168e90b3372c220011ffdbe4e795570e9ffc1ae
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97229682"
---
# <a name="_ismbbprint-_ismbbprint_l"></a>_ismbbprint, _ismbbprint_l

Определяет, является ли указанный многобайтовой символ печатным символом.

## <a name="syntax"></a>Синтаксис

```C
int _ismbbprint(
   unsigned int c
);
int _ismbbprint_l(
   unsigned int c,
   _locale_t locale
);
```

### <a name="parameters"></a>Параметры

*c*<br/>
Целое число, которое требуется проверить.

*locale*<br/>
Используемый языковой стандарт.

## <a name="return-value"></a>Возвращаемое значение

**_ismbbprint** возвращает ненулевое значение, если выражение:

`isprint(c) || _ismbbkprint(c)`

параметр имеет ненулевое значение для *языка c* или значение 0, если нет. **_ismbbprint** использует текущий языковой стандарт для любого поведения, зависящего от языкового стандарта. **_ismbbprint_l** является идентичным, за исключением того, что использует переданный языковой стандарт. Для получения дополнительной информации см. [Locale](../../c-runtime-library/locale.md).

## <a name="remarks"></a>Комментарии

По умолчанию глобальное состояние этой функции ограничивается приложением. Чтобы изменить это, см. раздел [глобальное состояние в CRT](../global-state.md).

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|**_ismbbprint**|\<mbctype.h>|
|**_ismbbprint_l**|\<mbctype.h>|

Дополнительные сведения о совместимости см. в разделе [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="see-also"></a>См. также раздел

[Классификация байтов](../../c-runtime-library/byte-classification.md)<br/>
[подпрограммы _ismbb](../../c-runtime-library/ismbb-routines.md)<br/>
