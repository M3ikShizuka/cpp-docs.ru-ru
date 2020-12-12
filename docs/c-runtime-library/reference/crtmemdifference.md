---
description: 'Дополнительные сведения: _CrtMemDifference'
title: _CrtMemDifference
ms.date: 11/04/2016
api_name:
- _CrtMemDifference
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
- _CrtMemDifference
- CrtMemDifference
helpviewer_keywords:
- CrtMemDifference function
- _CrtMemDifference function
ms.assetid: 0f327278-b551-482f-958b-76941f796ba4
ms.openlocfilehash: 076cead5f60df457171bbcdf2fd8690f0361870b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97319655"
---
# <a name="_crtmemdifference"></a>_CrtMemDifference

Сравнивает два состояния памяти и возвращает их различия (только отладочная версия).

## <a name="syntax"></a>Синтаксис

```C
int _CrtMemDifference(
   _CrtMemState *stateDiff,
   const _CrtMemState *oldState,
   const _CrtMemState *newState
);
```

### <a name="parameters"></a>Параметры

*статедифф*<br/>
Указатель на структуру **_CrtMemState** , которая используется для хранения различий между двумя состояниями памяти (возвращаемые).

*олдстате*<br/>
Указатель на более раннее состояние памяти (структура **_CrtMemState** ).

*Новое_состояние*<br/>
Указатель на более позднее состояние памяти (структура **_CrtMemState** ).

## <a name="return-value"></a>Возвращаемое значение

Если состояния памяти значительно отличаются, **_CrtMemDifference** возвращает значение true. В противном случае функция возвращает значение FALSE.

## <a name="remarks"></a>Комментарии

Функция **_CrtMemDifference** сравнивает *олдстате* и *NewState* и сохраняет их различия в *статедифф*, которые затем могут использоваться приложением для обнаружения утечек памяти и других проблем с памятью. Если [_DEBUG](../../c-runtime-library/debug.md) не определено, вызовы **_CrtMemDifference** удаляются во время предварительной обработки.

*NewState* и *олдстате* должны быть допустимыми указателями на структуру **_CrtMemState** , определенную в файле Crtdbg. h, которая была заполнена [_CrtMemCheckpoint](crtmemcheckpoint.md) перед вызовом **_CrtMemDifference**. *статедифф* должен быть указателем на ранее выделенный экземпляр структуры **_CrtMemState** . Если *статедифф*, *NewState* или *олдстате* имеет **значение NULL**, вызывается обработчик недопустимых параметров, как описано в разделе [Проверка параметров](../../c-runtime-library/parameter-validation.md). Если выполнение может быть продолжено, в параметре " [_doserrno", "_sys_errlist" и _sys_nerr](../../c-runtime-library/errno-doserrno-sys-errlist-and-sys-nerr.md) задано значение " **еинвал** ", а функция возвращает false.

**_CrtMemDifference** сравнивает значения полей **_CrtMemState** блоков в *олдстате* с ними в *NewState* и сохраняет результат в *статедифф*. Если количество выделенных типов блоков или общее количество выделенных блоков каждого типа различается в двух состояниях памяти, считается, что состояния значительно отличаются. Разница между наибольшим объемом, когда-либо выделено за один раз для двух состояний, и разность между общими распределениями для двух состояний также хранится в *статедифф*.

По умолчанию внутренние блоки времени выполнения C (**_CRT_BLOCK**) не включаются в операции состояния памяти. Функцию [_CrtSetDbgFlag](crtsetdbgflag.md) можно использовать, чтобы включить **_CRTDBG_CHECK_CRT_DF** бит **_crtDbgFlag** , чтобы включить эти блоки в обнаружение утечек и другие операции состояния памяти. Освобожденные блоки памяти (**_FREE_BLOCK**) не приводят к тому, что **_CrtMemDifference** возвращают значение true.

Дополнительные сведения о функциях состояния кучи и структуре **_CrtMemState** см. в разделе [функции создания отчетов о состоянии кучи](/visualstudio/debugger/crt-debug-heap-details). Сведения о выделении, инициализации и управлении блоками памяти в отладочной версии базовой кучи, см. в статье [CRT Debug Heap Details](/visualstudio/debugger/crt-debug-heap-details).

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|Необязательный заголовок|
|-------------|---------------------|---------------------|
|**_CrtMemDifference**|\<crtdbg.h>|\<errno.h>|

Дополнительные сведения о совместимости см. в разделе [Compatibility](../../c-runtime-library/compatibility.md).

**Библиотеки:** только отладочные версии [функций библиотеки CRT](../../c-runtime-library/crt-library-features.md).

## <a name="see-also"></a>См. также раздел

[Отладочные подпрограммы](../../c-runtime-library/debug-routines.md)<br/>
[_crtDbgFlag](../../c-runtime-library/crtdbgflag.md)<br/>
