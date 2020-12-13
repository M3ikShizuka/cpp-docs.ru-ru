---
description: Дополнительные сведения об непредвиденных действиях (CRT)
title: unexpected (CRT)
ms.date: 11/04/2016
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
api_type:
- DLLExport
topic_type:
- apiref
f1_keywords:
- unexpected
helpviewer_keywords:
- unexpected function
ms.assetid: 2f873763-15ad-4556-a924-dcf28f2b52b4
ms.openlocfilehash: 73c632c4dd5bfedbb1c3724e60786b348f77f0be
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97186640"
---
# <a name="unexpected-crt"></a>unexpected (CRT)

Вызывает **Terminate** или функцию, указанную с помощью **set_unexpected**.

## <a name="syntax"></a>Синтаксис

```C
void unexpected( void );
```

## <a name="remarks"></a>Remarks

**Непредвиденная** подпрограммы не используется с текущей реализацией обработки исключений C++. **неожиданные** вызовы **завершаются** по умолчанию. Это поведение по умолчанию можно изменить, написав пользовательскую функцию завершения и вызвав **set_unexpected** с именем функции в качестве аргумента. **непредвиденный** вызов последней функции, заданной в качестве аргумента для **set_unexpected**.

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|**известно**|\<eh.h>|

Дополнительные сведения о совместимости см. в статье [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="see-also"></a>См. также раздел

[Подпрограммы обработки исключений](../../c-runtime-library/exception-handling-routines.md)<br/>
[рвал](abort.md)<br/>
[_set_se_translator](set-se-translator.md)<br/>
[set_terminate](set-terminate-crt.md)<br/>
[set_unexpected](set-unexpected-crt.md)<br/>
[заканчива](terminate-crt.md)<br/>
