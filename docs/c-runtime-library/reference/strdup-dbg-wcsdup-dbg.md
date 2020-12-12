---
description: 'Дополнительные сведения: _strdup_dbg, _wcsdup_dbg'
title: _strdup_dbg, _wcsdup_dbg
ms.date: 11/04/2016
api_name:
- _strdup_dbg
- _wcsdup_dbg
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
- _wcsdup_dbg
- strdup_dbg
- _strdup_dbg
- wcsdup_dbg
helpviewer_keywords:
- _wcsdup_dbg function
- stdup_dbg function
- copying strings
- duplicating strings
- strings [C++], copying
- strings [C++], duplicating
- _strdup_dbg function
- wcsdup_dbg function
ms.assetid: 681db70c-d124-43ab-b83e-5eeea9035097
ms.openlocfilehash: c7001d7948f733977213267fdabd9faee4ddffd4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97322486"
---
# <a name="_strdup_dbg-_wcsdup_dbg"></a>_strdup_dbg, _wcsdup_dbg

Версии [_strdup и _wcsdup](strdup-wcsdup-mbsdup.md) , которые используют отладочную версию **malloc**.

## <a name="syntax"></a>Синтаксис

```C
char *_strdup_dbg(
   const char *strSource,
   int blockType,
   const char *filename,
   int linenumber
);
wchar_t *_wcsdup_dbg(
   const wchar_t *strSource,
   int blockType,
   const char *filename,
   int linenumber
);
```

### <a name="parameters"></a>Параметры

*стрсаурце*<br/>
Исходная строка, завершающаяся символом NULL.

*blockType*<br/>
Запрошенный тип блока памяти: **_CLIENT_BLOCK** или **_NORMAL_BLOCK**.

*filename*<br/>
Указатель на имя исходного файла, который запросил операцию выделения, или **значение NULL**.

*LineNumber*<br/>
Номер строки в исходном файле, где была запрошена операция выделения, или **значение NULL**.

## <a name="return-value"></a>Возвращаемое значение

Каждая из этих функций возвращает указатель на место хранения копируемой строки или **значение NULL** , если не удается выделить хранилище.

## <a name="remarks"></a>Комментарии

Функции **_strdup_dbg** и **_wcsdup_dbg** идентичны **_strdup** и **_wcsdup** за исключением того, что при определении **_DEBUG** эти функции используют отладочную версию **malloc**, **_malloc_dbg**, чтобы выделить память для дублирования строки. Сведения о возможностях отладки **_malloc_dbg** см. в разделе [_malloc_dbg](malloc-dbg.md).

Как правило, явно вызывать эти функции не требуется. Вместо этого можно определить флаг **_CRTDBG_MAP_ALLOC**. Если определено **_CRTDBG_MAP_ALLOC** , вызовы **_strdup** и **_wcsdup** пересопоставляются с **_strdup_dbg** и **_wcsdup_dbg** соответственно, с *блокктипе* , для которого задано значение **_NORMAL_BLOCK**. Таким образом, не нужно явно вызывать эти функции, если не нужно помечать блоки кучи как **_CLIENT_BLOCK**. Дополнительные сведения о типах блоков см. в разделе [Типы блоков в отладочной куче](/visualstudio/debugger/crt-debug-heap-details).

### <a name="generic-text-routine-mappings"></a>Универсальное текстовое сопоставление функций

|Подпрограмма TCHAR.H|_UNICODE и _MBCS не определены|_MBCS определено|_UNICODE определено|
|---------------------|------------------------------------|--------------------|-----------------------|
|**_tcsdup_dbg**|**_strdup_dbg**|**_mbsdup**|**_wcsdup_dbg**|

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|**_strdup_dbg**, **_wcsdup_dbg**|\<crtdbg.h>|

Дополнительные сведения о совместимости см. в статье [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="libraries"></a>Библиотеки

Все отладочные версии [библиотек времени выполнения C](../../c-runtime-library/crt-library-features.md).

## <a name="see-also"></a>См. также раздел

[Управление строками](../../c-runtime-library/string-manipulation-crt.md)<br/>
[_strdup, _wcsdup, _mbsdup](strdup-wcsdup-mbsdup.md)<br/>
[Версии отладки функций выделения кучи](/visualstudio/debugger/debug-versions-of-heap-allocation-functions)<br/>
