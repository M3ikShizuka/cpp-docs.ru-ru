---
description: 'Дополнительные сведения: _get_unexpected'
title: _get_unexpected
ms.date: 11/04/2016
api_name:
- _get_unexpected
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
- __get_unexpected
- _get_unexpected
- get_unexpected
helpviewer_keywords:
- __get_unexpected function
- get_unexpected function
- _get_unexpected function
ms.assetid: a5f7a7a0-18e0-485e-953d-db291068a1e8
ms.openlocfilehash: 9c8f21815aa465e1325ef0519ba21abb1e506db3
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97338939"
---
# <a name="_get_unexpected"></a>_get_unexpected

Возвращает подпрограммы завершения, вызываемую **непредвиденным**.

## <a name="syntax"></a>Синтаксис

```C
unexpected_function _get_unexpected( void );
```

## <a name="return-value"></a>Возвращаемое значение

Возвращает указатель на функцию, зарегистрированную функцией [set_unexpected](set-unexpected-crt.md). Если функция не задана, возвращаемое значение может использоваться для восстановления поведения по умолчанию; Это значение может быть **равно NULL**.

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|**_get_unexpected**|\<eh.h>|

Дополнительные сведения о совместимости см. в статье [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="see-also"></a>См. также раздел

[Подпрограммы обработки исключений](../../c-runtime-library/exception-handling-routines.md)<br/>
[рвал](abort.md)<br/>
[set_terminate](set-terminate-crt.md)<br/>
[заканчива](terminate-crt.md)<br/>
[известно](unexpected-crt.md)<br/>
