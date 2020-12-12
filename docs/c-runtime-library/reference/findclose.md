---
description: 'Дополнительные сведения: _findclose'
title: _findclose
ms.date: 4/2/2020
api_name:
- _findclose
- _o__findclose
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
- api-ms-win-crt-filesystem-l1-1-0.dll
- api-ms-win-crt-private-l1-1-0.dll
api_type:
- DLLExport
topic_type:
- apiref
f1_keywords:
- _findclose
- findclose
helpviewer_keywords:
- _findclose function
- findclose function
ms.assetid: 9216c573-0878-444c-b5d7-cdaf16fb9163
ms.openlocfilehash: 389a8aaf55605a1d9e3193c86ce500bf313fd631
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97329196"
---
# <a name="_findclose"></a>_findclose

Закрывает указанный дескриптор поиска и освобождает связанные ресурсы.

## <a name="syntax"></a>Синтаксис

```C
int _findclose(
   intptr_t handle
);
```

### <a name="parameters"></a>Параметры

*справиться*<br/>
Маркер поиска, возвращенный предыдущим вызовом метода **_findfirst**.

## <a name="return-value"></a>Возвращаемое значение

В случае успеха **_findclose** возвращает 0. В противном случае возвращается значение-1 **и устанавливается значение** **еноент**, указывающее, что больше не удалось найти соответствующие файлы.

## <a name="remarks"></a>Комментарии

По умолчанию глобальное состояние этой функции ограничивается приложением. Чтобы изменить это, см. раздел [глобальное состояние в CRT](../global-state.md).

## <a name="requirements"></a>Требования

|Функция|Обязательный заголовок|
|--------------|---------------------|
|**_findclose**|\<io.h>|

Дополнительные сведения о совместимости см. в разделе [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="see-also"></a>См. также раздел

[Системные вызовы](../../c-runtime-library/system-calls.md)<br/>
[Функции поиска имен файлов](../../c-runtime-library/filename-search-functions.md)<br/>
