---
description: 'Дополнительные сведения: _CrtIsMemoryBlock'
title: _CrtIsMemoryBlock
ms.date: 11/04/2016
api_name:
- _CrtIsMemoryBlock
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
- CrtlsMemoryBlock
- _CrtIsMemoryBlock
helpviewer_keywords:
- _CrtIsMemoryBlock function
- CrtIsMemoryBlock function
ms.assetid: f7cbbc60-3690-4da0-a07b-68fd7f250273
ms.openlocfilehash: 81a4b515461a45f566f95728180013408ccda43a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97319720"
---
# <a name="_crtismemoryblock"></a>_CrtIsMemoryBlock

Проверяет, находится ли указанный блок памяти в локальной куче и имеет ли он действительный идентификатор типа блока отладочной кучи (только в отладочной версии).

## <a name="syntax"></a>Синтаксис

```C
int _CrtIsMemoryBlock(
   const void *userData,
   unsigned int size,
   long *requestNumber,
   char **filename,
   int *linenumber
);
```

### <a name="parameters"></a>Параметры

*userData*<br/>
Указатель на начало блока памяти, требующего проверки.

*size*<br/>
Размер указанного блока в байтах.

*рекуестнумбер*<br/>
Указатель на номер выделения блока или **значение NULL**.

*filename*<br/>
Указатель на имя исходного файла, который запросил блок, или **значение NULL**.

*LineNumber*<br/>
Указатель на номер строки в исходном файле или **значение NULL**.

## <a name="return-value"></a>Возвращаемое значение

**_CrtIsMemoryBlock** возвращает **значение true** , если указанный блок памяти находится в локальной куче и имеет допустимый идентификатор типа блока отладочной кучи. в противном случае функция возвращает **значение false**.

## <a name="remarks"></a>Комментарии

Функция **_CrtIsMemoryBlock** проверяет, находится ли указанный блок памяти в локальной куче приложения и имеет ли он допустимый идентификатор типа блока. Эту функцию можно также использовать для получения порядкового номера распределения объекта, а также имени или номера строки исходного файла, содержащего исходный запрос на выделение блока памяти. Передача значений, отличных от **null** , для параметров *рекуестнумбер*, *filename* или *LineNumber* приводит к тому, что **_CrtIsMemoryBlock** задают эти параметры значениям в заголовке отладки блока памяти, если он находит блок в локальной куче. Если [_DEBUG](../../c-runtime-library/debug.md) не определено, вызовы **_CrtIsMemoryBlock** удаляются во время предварительной обработки.

Если **_CrtIsMemoryBlock** завершается ошибкой, возвращается **значение false** , и выходные параметры инициализируются значениями по умолчанию: *рекуестнумбер* и **LineNumber** имеют значение 0, а *filename* имеет значение **null**.

Поскольку эта функция возвращает **значение true** или **false**, ее можно передать в один из [_ASSERTных](assert-asserte-assert-expr-macros.md) макросов, чтобы создать простой механизм обработки ошибок отладки. Приведенный ниже пример вызывает сбой утверждения, если указанный адрес находится не в локальной куче.

```C
_ASSERTE( _CrtIsMemoryBlock( userData, size, &requestNumber,
          &filename, &linenumber ) );
```

Дополнительные сведения о том, как **_CrtIsMemoryBlock** можно использовать с другими функциями и макросами отладки, см. в разделе [macros for Reporting](/visualstudio/debugger/macros-for-reporting). Сведения о выделении, инициализации и управлении блоками памяти в отладочной версии базовой кучи, см. в статье [CRT Debug Heap Details](/visualstudio/debugger/crt-debug-heap-details).

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|**_CrtIsMemoryBlock**|\<crtdbg.h>|

Дополнительные сведения о совместимости см. в разделе [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="libraries"></a>Библиотеки

Только отладочные версии [библиотек времени выполнения языка C](../../c-runtime-library/crt-library-features.md).

## <a name="example"></a>Пример

См. пример для раздела [_CrtIsValidHeapPointer](crtisvalidheappointer.md).

## <a name="see-also"></a>См. также раздел

[Отладочные подпрограммы](../../c-runtime-library/debug-routines.md)<br/>
