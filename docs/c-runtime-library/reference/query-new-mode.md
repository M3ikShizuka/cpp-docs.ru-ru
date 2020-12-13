---
description: 'Дополнительные сведения: _query_new_mode'
title: _query_new_mode
ms.date: 11/04/2016
api_name:
- _query_new_mode
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
- api-ms-win-crt-heap-l1-1-0.dll
api_type:
- DLLExport
topic_type:
- apiref
f1_keywords:
- query_new_mode
- _query_new_mode
helpviewer_keywords:
- query_new_mode function
- handler modes
- _query_new_mode function
ms.assetid: e185c5f9-b73b-4257-8eff-b47648374768
ms.openlocfilehash: 90c7355f4babc4726c8b52d61309eb1ceb23c9a3
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97137141"
---
# <a name="_query_new_mode"></a>_query_new_mode

Возвращает целое число, указывающее новый режим обработчика, заданный **_set_new_mode** для **malloc**.

## <a name="syntax"></a>Синтаксис

```C
int _query_new_mode(
   void
);
```

## <a name="return-value"></a>Возвращаемое значение

Возвращает текущий новый режим обработчика, а именно 0 или 1 для **malloc**. Возвращаемое значение 1 указывает, что при сбое выделения памяти **malloc** вызывает новую подпрограммы обработчика; Возвращаемое значение 0 указывает, что это не так.

## <a name="remarks"></a>Комментарии

Функция **_Query_new_mode** c++ возвращает целое число, указывающее новый режим обработчика, заданный функцией [_set_new_mode](set-new-mode.md) C++ для [malloc](malloc.md). Новый режим обработчика показывает **, будет ли** при сбое выделения памяти вызывать новую подпрограммы обработчика, заданную [_set_new_handler](set-new-handler.md). По умолчанию **malloc** не вызывает новую подпрограммы обработчика при сбое. Можно использовать **_set_new_mode** , чтобы переопределить это поведение, чтобы в случае сбоя **malloc** вызовет новую подпрограммы обработчика так же, как это **`new`** делает оператор в случае сбоя выделения памяти. Дополнительные сведения см. в разделе о [новых и удаленных операторах](../../cpp/new-and-delete-operators.md) справочника по языку C++.

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|**_query_new_mode**|\<new.h>|

Дополнительные сведения о совместимости см. в разделе [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="libraries"></a>Библиотеки

Все версии [библиотек времени выполнения языка C](../../c-runtime-library/crt-library-features.md).

## <a name="see-also"></a>См. также раздел

[Выделение памяти](../../c-runtime-library/memory-allocation.md)<br/>
[calloc](calloc.md)<br/>
[free](free.md)<br/>
[realloc](realloc.md)<br/>
[_query_new_handler](query-new-handler.md)<br/>
