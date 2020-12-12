---
description: 'Дополнительные сведения: __uncaught_exception'
title: __uncaught_exception
ms.date: 11/04/2016
api_name:
- __uncaught_exception
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
- __uncaught_exception
helpviewer_keywords:
- __uncaught_exception
ms.assetid: 4d9b75c6-c9c7-4876-b761-ea9ab1925e96
ms.openlocfilehash: 22417e10e96e70faf2754ae2d8bb03b90bdbe020
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97124817"
---
# <a name="__uncaught_exception"></a>__uncaught_exception

Указывает, было ли создано одно или несколько исключений, но пока они не были обработаны соответствующим **`catch`** блоком инструкции [try-catch](../../cpp/try-throw-and-catch-statements-cpp.md) .

## <a name="syntax"></a>Синтаксис

```cpp
bool __uncaught_exception(
   );
```

## <a name="return-value"></a>Возвращаемое значение

**`true`** с момента возникновения исключения в **`try`** блоке до **`catch`** инициализации соответствующего блока; в противном случае — значение **`false`** .

## <a name="remarks"></a>Remarks

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|__uncaught_exception|eh.h|

## <a name="see-also"></a>См. также раздел

[Операторы try, throw и catch (C++)](../../cpp/try-throw-and-catch-statements-cpp.md)<br/>
