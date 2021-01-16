---
description: Дополнительные сведения об непредвиденных действиях (CRT)
title: unexpected (CRT)
ms.date: 1/14/2021
api_name:
- unexpected
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
- api-ms-win-crt-private-l1-1-0.dll
api_type:
- DLLExport
topic_type:
- apiref
f1_keywords:
- unexpected
helpviewer_keywords:
- unexpected function
ms.assetid: 2f873763-15ad-4556-a924-dcf28f2b52b4
ms.openlocfilehash: 098d686e7c33d17020990b1db168d95c327d5112
ms.sourcegitcommit: 1cd8f8a75fd036ffa57bc70f3ca869042d8019d4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "98242908"
---
# <a name="unexpected-crt"></a>`unexpected` Электрон

Вызывает **`terminate`** или функцию, указанную с помощью **`set_unexpected`** .

## <a name="syntax"></a>Синтаксис

```C
void unexpected( void );
```

## <a name="remarks"></a>Remarks

**`unexpected`** Подпрограммы не используются с текущей реализацией обработки исключений C++. **`unexpected`** вызовы по **`terminate`** умолчанию. Это поведение по умолчанию можно изменить, написав пользовательскую функцию завершения. Вызовите **`set_unexpected`** функцию с именем функции в качестве аргумента. **`unexpected`** вызывает последнюю функцию, переданную в **`set_unexpected`** .

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|**`unexpected`**|`<eh.h>`|

Дополнительные сведения о совместимости см. в разделе [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="see-also"></a>См. также

[Подпрограммы обработки исключений](../../c-runtime-library/exception-handling-routines.md)<br/>
[рвал](abort.md)<br/>
[_set_se_translator](set-se-translator.md)<br/>
[set_terminate](set-terminate-crt.md)<br/>
[set_unexpected](set-unexpected-crt.md)<br/>
[заканчива](terminate-crt.md)<br/>
