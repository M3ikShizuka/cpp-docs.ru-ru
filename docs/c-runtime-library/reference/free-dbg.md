---
description: 'Дополнительные сведения: _free_dbg'
title: _free_dbg
ms.date: 11/04/2016
api_name:
- _free_dbg
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
- _free_dbg
- free_dbg
helpviewer_keywords:
- memory blocks, deallocating
- freeing memory
- _free_dbg function
- free_dbg function
ms.assetid: fc5e8299-616d-48a0-b979-e037117278c6
ms.openlocfilehash: 4baba591349c197b301b0dcd11b1998adfc7a971
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97314039"
---
# <a name="_free_dbg"></a>_free_dbg

Освобождает блок памяти в куче (только в отладочной версии).

## <a name="syntax"></a>Синтаксис

```C
void _free_dbg(
   void *userData,
   int blockType
);
```

### <a name="parameters"></a>Параметры

*userData*<br/>
Указатель на выделенный блок памяти, который требуется освободить.

*blockType*<br/>
Тип выделенного блока памяти, который должен быть освобожден: **_CLIENT_BLOCK**, **_NORMAL_BLOCK** или **_IGNORE_BLOCK**.

## <a name="remarks"></a>Комментарии

Функция **_free_dbg** является отладочной версией функции [Free](free.md) . Если [_DEBUG](../../c-runtime-library/debug.md) не определен, каждый вызов **_free_dbg** сокращается до вызова функции **Free**. **Свободные** и **_free_dbg** освобождают блок памяти в базовой куче, но **_free_dbg** поддерживает две функции отладки: возможность сохранения освобожденных блоков в связанном списке кучи для имитации нехватки памяти и параметра типа блока для освобождения конкретных типов выделения.

**_free_dbg** выполняет проверку допустимости для всех указанных файлов и расположений блоков перед выполнением бесплатной операции. Приложение не ожидает предоставления этих сведений. Когда освобождается блок памяти, диспетчер отладочной кучи автоматически проверяет целостность буферов по обеим сторонам пользовательской части и выдает отчет об ошибке в случае их перезаписи. Если задано битовое поле **_CRTDBG_DELAY_FREE_MEM_DF** флага [_crtDbgFlag](../../c-runtime-library/crtdbgflag.md) , освобожденный блок заполняется значением 0xDD, ему назначается тип блока **_FREE_BLOCK** и хранится в связанном списке блоков памяти кучи.

Если при освобождении памяти произошла ошибка, то параметру "очистить" **задается** информация из операционной системы о характере сбоя. Дополнительные сведения см. в разделе [errno, _doserrno, _sys_errlist и _sys_nerr](../../c-runtime-library/errno-doserrno-sys-errlist-and-sys-nerr.md).

Сведения о выделении, инициализации и управлении блоками памяти в отладочной версии базовой кучи, см. в статье [CRT Debug Heap Details](/visualstudio/debugger/crt-debug-heap-details). Сведения о типах блоков выделения и их использовании см. в разделе [типы блоков в отладочной куче](/visualstudio/debugger/crt-debug-heap-details). Сведения о различиях между вызовом стандартной функции кучи и ее отладочной версии в сборке отладки приложения см. в разделе [Версии отладки функций выделения кучи](/visualstudio/debugger/debug-versions-of-heap-allocation-functions).

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|**_free_dbg**|\<crtdbg.h>|

Дополнительные сведения о совместимости см. в разделе [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="example"></a>Пример

Пример использования **_free_dbg** см. в разделе [crt_dbg2](https://github.com/Microsoft/VCSamples/tree/master/VC2010Samples/crt/crt_dbg2).

## <a name="see-also"></a>См. также раздел

[Отладочные подпрограммы](../../c-runtime-library/debug-routines.md)<br/>
[_malloc_dbg](malloc-dbg.md)<br/>
