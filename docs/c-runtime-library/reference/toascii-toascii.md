---
description: 'Дополнительные сведения о: toascii, __toascii'
title: toascii, __toascii
ms.date: 11/04/2016
api_name:
- __toascii
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
- api-ms-win-crt-convert-l1-1-0.dll
api_type:
- DLLExport
topic_type:
- apiref
f1_keywords:
- __toascii
- toascii
- ctype/toascii
- ctype/__toascii
helpviewer_keywords:
- toascii function
- string conversion, to ASCII characters
- __toascii function
- ASCII characters, converting to
ms.assetid: a07c0608-b0e2-4da2-a20c-7b64d6a9b77c
ms.openlocfilehash: 9f1718da5e7d701bb6cc6ea68c1e21b6fe4283f2
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97318355"
---
# <a name="toascii-__toascii"></a>toascii, __toascii

Преобразуют символы в 7-разрядный код ASCII методом усечения.

## <a name="syntax"></a>Синтаксис

```C
int __toascii(
   int c
);
#define toascii __toascii
```

### <a name="parameters"></a>Параметры

*c*<br/>
Символ для преобразования.

## <a name="return-value"></a>Возвращаемое значение

**__toascii** преобразует значение *c* в 7-разрядный диапазон ASCII и возвращает результат. Возвращаемое значение для указания ошибки не зарезервировано.

## <a name="remarks"></a>Комментарии

**__Toascii** подпрограммы Преобразует заданный символ в символ ASCII, округляя его до 7 младших битов. Никакие другие преобразования не применяются.

**__Toascii** процедура определяется как макрос, если не определен _CTYPE_DISABLE_MACROS макроса препроцессора. В целях обратной совместимости **toascii** определяется как макрос, только если [&#95;&#95;&#95;&#95;STDC](../../preprocessor/predefined-macros.md) не определена или определен как 0. в противном случае он не определен.

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|**toascii**, **__toascii**|Ц \<ctype.h><br /><br /> C++: \<cctype> или \<ctype.h>|

Макрос **toascii** является расширением POSIX, а **__toascii** является реализацией модуля POSIX для Microsoft. Дополнительные сведения о совместимости см. в статье [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="see-also"></a>См. также раздел

[Преобразование данных](../../c-runtime-library/data-conversion.md)<br/>
[является, подпрограммы isw](../../c-runtime-library/is-isw-routines.md)<br/>
[в функции](../../c-runtime-library/to-functions.md)<br/>
