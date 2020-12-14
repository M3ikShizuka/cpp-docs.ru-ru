---
description: 'Дополнительные сведения: _free_locale'
title: _free_locale
ms.date: 4/2/2020
api_name:
- _free_locale
- _o__free_locale
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
- api-ms-win-crt-locale-l1-1-0.dll
- api-ms-win-crt-private-l1-1-0.dll
api_type:
- DLLExport
topic_type:
- apiref
f1_keywords:
- __free_locale
- free_locale
- _free_locale
helpviewer_keywords:
- __free_locale function
- free_locale function
- locales, freeing
- _free_locale function
ms.assetid: 1f08d348-ab32-4028-a145-6cbd51b49af9
ms.openlocfilehash: 441686a1ee037097c164ae60b4ccc418f0d38ac8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97211275"
---
# <a name="_free_locale"></a>_free_locale

Освобождает объект языкового стандарта.

## <a name="syntax"></a>Синтаксис

```C
void _free_locale(
   _locale_t locale
);
```

### <a name="parameters"></a>Параметры

*locale*<br/>
Объект языкового стандарта, который необходимо освободить.

## <a name="remarks"></a>Комментарии

Функция **_free_locale** используется для высвобождения объекта языкового стандарта, полученного из вызова метода **_get_current_locale** или **_create_locale**.

Предыдущее имя этой функции, **__free_locale** (с двумя символами подчеркивания в начале), не рекомендуется к использованию.

По умолчанию глобальное состояние этой функции ограничивается приложением. Чтобы изменить это, см. раздел [глобальное состояние в CRT](../global-state.md).

## <a name="requirements"></a>Требования

|**Подпрограмма**|Обязательный заголовок|
|---------------|---------------------|
|**_free_locale**|\<locale.h>|

Дополнительные сведения о совместимости см. в разделе [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="see-also"></a>См. также раздел

[_get_current_locale](get-current-locale.md)<br/>
[_create_locale, _wcreate_locale](create-locale-wcreate-locale.md)<br/>
