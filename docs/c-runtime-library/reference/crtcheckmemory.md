---
description: 'Дополнительные сведения: _CrtCheckMemory'
title: _CrtCheckMemory
ms.date: 11/04/2016
api_name:
- _CrtCheckMemory
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
- CrtCheckMemory
- _CrtCheckMemory
helpviewer_keywords:
- _CrtCheckMemory function
- CrtCheckMemory function
ms.assetid: 457cc72e-60fd-4177-ab5c-6ae26a420765
ms.openlocfilehash: f2537997a9adc1c2346560d3b65eecc633933616
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97221596"
---
# <a name="_crtcheckmemory"></a>_CrtCheckMemory

Проверяет целостность выделенных блоков памяти в отладочной куче (только в отладочной версии).

## <a name="syntax"></a>Синтаксис

```C

int _CrtCheckMemory( void );
```

## <a name="return-value"></a>Возвращаемое значение

В случае успеха **_CrtCheckMemory** возвращает значение true; в противном случае функция возвращает значение FALSE.

## <a name="remarks"></a>Комментарии

Функция **_CrtCheckMemory** проверяет память, выделенную диспетчером отладочной кучи, проверяя базовую кучу и проверяя каждый блок памяти. Если ошибка или несоответствие памяти обнаружены в базовой куче, сведениях заголовка отладки или буферах перезаписи, **_CrtCheckMemory** создает отчет об отладке с информацией, описывающей условие ошибки. Если [_DEBUG](../../c-runtime-library/debug.md) не определено, вызовы **_CrtCheckMemory** удаляются во время предварительной обработки.

Поведение **_CrtCheckMemory** может контролироваться путем установки битовых полей флага [_crtDbgFlag](../../c-runtime-library/crtdbgflag.md) с помощью функции [_CrtSetDbgFlag](crtsetdbgflag.md) . Включение **_CRTDBG_CHECK_ALWAYS_DF** битового поля для результатов **_CrtCheckMemory** вызывается каждый раз, когда запрашивается операция выделения памяти. Несмотря на то, что этот метод замедляет выполнение, он позволяет быстро перехватывать ошибки. Отключение **_CRTDBG_ALLOC_MEM_DF** битового поля приведет к тому, что **_CrtCheckMemory** не будет проверять кучу и немедленно возвращать **значение true**.

Поскольку эта функция возвращает **значение true** или **false**, ее можно передать в один из [_ASSERTных](assert-asserte-assert-expr-macros.md) макросов, чтобы создать простой механизм обработки ошибок отладки. Следующий пример вызывает сбой утверждения, если в куче обнаружено повреждение.

```C
_ASSERTE( _CrtCheckMemory( ) );
```

Дополнительные сведения о том, как **_CrtCheckMemory** можно использовать с другими функциями отладки, см. в разделе [функции создания отчетов о состоянии кучи](/visualstudio/debugger/crt-debug-heap-details). Общие сведения об управлении памятью и отладочной куче см. в разделе [Сведения о куче отладки CRT](/visualstudio/debugger/crt-debug-heap-details).

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|**_CrtCheckMemory**|\<crtdbg.h>|

Дополнительные сведения о совместимости см. в разделе [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="libraries"></a>Библиотеки

Только отладочные версии [библиотек времени выполнения языка C](../../c-runtime-library/crt-library-features.md).

## <a name="example"></a>Пример

Пример использования **_CrtCheckMemory** см. в разделе [crt_dbg1](https://github.com/Microsoft/VCSamples/tree/master/VC2010Samples/crt/crt_dbg1).

## <a name="see-also"></a>См. также раздел

[Отладочные подпрограммы](../../c-runtime-library/debug-routines.md)<br/>
[_crtDbgFlag](../../c-runtime-library/crtdbgflag.md)<br/>
[_CrtSetDbgFlag](crtsetdbgflag.md)<br/>
