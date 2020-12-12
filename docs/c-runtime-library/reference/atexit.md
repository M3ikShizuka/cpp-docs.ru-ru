---
description: 'Дополнительные сведения о: atexit'
title: atexit
ms.date: 11/04/2016
api_name:
- atexit
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
- atexit
helpviewer_keywords:
- processing, at exit
- atexit function
ms.assetid: 92c156d2-8052-4e58-96dc-00128baac6f9
ms.openlocfilehash: 82c0bbfdb9af62faff9239781b5db340183e25fa
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97117540"
---
# <a name="atexit"></a>atexit

Обрабатывает указанную функцию на выходе.

## <a name="syntax"></a>Синтаксис

```C
int atexit(
   void (__cdecl *func )( void )
);
```

### <a name="parameters"></a>Параметры

*func*<br/>
Функция, которую требуется вызвать.

## <a name="return-value"></a>Возвращаемое значение

**atexit** возвращает 0 в случае успеха или ненулевое значение при возникновении ошибки.

## <a name="remarks"></a>Комментарии

Функции **atexit** передается адрес функции *Func* , которая вызывается, когда программа завершается нормально. Последовательные вызовы **atexit** создают регистр функций, которые выполняются в порядке "последним по, первым обслужен" (ЛИФО). Функции, передаваемые в **atexit** , не могут принимать параметры. **atexit** и **_onexit** использовать кучу для хранения регистра функций. В связи с этим количество функций, которое можно зарегистрировать, ограничивается только памятью кучи.

Код функции **atexit** не должен содержать зависимости от любой библиотеки DLL, которая могла быть уже выгружена при вызове функции **atexit** .

Чтобы создать приложение, совместимое с ANSI, используйте стандартную функцию **ATEXIT** ANSI (вместо аналогичной функции **_onexit** ).

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|**atexit**|\<stdlib.h>|

## <a name="example"></a>Пример

Эта программа отправляет четыре функции в стек функций, которые должны выполняться при вызове **atexit** . При завершении работы программы эти программы выполняются в обратном порядке.

```C
// crt_atexit.c
#include <stdlib.h>
#include <stdio.h>

void fn1( void ), fn2( void ), fn3( void ), fn4( void );

int main( void )
{
   atexit( fn1 );
   atexit( fn2 );
   atexit( fn3 );
   atexit( fn4 );
   printf( "This is executed first.\n" );
}

void fn1()
{
   printf( "next.\n" );
}

void fn2()
{
   printf( "executed " );
}

void fn3()
{
   printf( "is " );
}

void fn4()
{
   printf( "This " );
}
```

```Output
This is executed first.
This is executed next.
```

## <a name="see-also"></a>См. также раздел

[Управление процессами и средой](../../c-runtime-library/process-and-environment-control.md)<br/>
[рвал](abort.md)<br/>
[exit, _Exit, _exit](exit-exit-exit.md)<br/>
[_onexit, _onexit_m](onexit-onexit-m.md)<br/>
