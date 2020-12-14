---
description: 'Дополнительные сведения о: setbuf'
title: setbuf
ms.date: 4/2/2020
api_name:
- setbuf
- _o_setbuf
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
- api-ms-win-crt-stdio-l1-1-0.dll
- api-ms-win-crt-private-l1-1-0.dll
api_type:
- DLLExport
topic_type:
- apiref
f1_keywords:
- setbuf
helpviewer_keywords:
- setbuf function
- stream buffering
ms.assetid: 13beda22-7b56-455d-8a6c-f2eb636885b9
ms.openlocfilehash: 756cb09fb35ed6e8cf6369f20693e2f0f0b7acaa
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97211067"
---
# <a name="setbuf"></a>setbuf

Управляет буферизацией потока. Эта функция не рекомендуется; вместо нее используйте функцию [setvbuf](setvbuf.md) .

## <a name="syntax"></a>Синтаксис

```C
void setbuf(
   FILE *stream,
   char *buffer
);
```

### <a name="parameters"></a>Параметры

*вышестоящий*<br/>
Указатель на структуру **FILE**.

*двойной*<br/>
Выделенный пользователем буфер.

## <a name="remarks"></a>Комментарии

Функция **setbuf** управляет буферизацией *потока*. Аргумент *потока* должен ссылаться на открытый файл, который еще не был прочитан или не записан. Если аргумент *buffer* имеет **значение NULL**, поток не буферизован. В противном случае буфер должен указывать на массив символов длины **буфсиз**, где **буфсиз** — размер буфера, как определено в stdio. H. Вместо буфера, по умолчанию выделенного системой для данного потока, для буферизации ввода-вывода используется указанный пользователем буфер. Поток **stderr** по умолчанию не буферизован, но можно использовать **setbuf** для назначения буферов в **stderr**.

**setbuf** был заменен [setvbuf](setvbuf.md), который является предпочтительной подпрограммой для нового кода. В отличие от **setvbuf**, **setbuf** не может сообщать об ошибках. **setvbuf** также позволяет управлять режимом буферизации и размером буфера. **setbuf** существует для совместимости с существующим кодом.

По умолчанию глобальное состояние этой функции ограничивается приложением. Чтобы изменить это, см. раздел [глобальное состояние в CRT](../global-state.md).

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|**setbuf**|\<stdio.h>|

Дополнительные сведения о совместимости см. в статье [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="example"></a>Пример

```C
// crt_setbuf.c
// compile with: /W3
// This program first opens files named DATA1 and
// DATA2. Then it uses setbuf to give DATA1 a user-assigned
// buffer and to change DATA2 so that it has no buffer.

#include <stdio.h>

int main( void )
{
   char buf[BUFSIZ];
   FILE *stream1, *stream2;

   fopen_s( &stream1, "data1", "a" );
   fopen_s( &stream2, "data2", "w" );

   if( (stream1 != NULL) && (stream2 != NULL) )
   {
      // "stream1" uses user-assigned buffer:
      setbuf( stream1, buf ); // C4996
      // Note: setbuf is deprecated; consider using setvbuf instead
      printf( "stream1 set to user-defined buffer at: %Fp\n", buf );

      // "stream2" is unbuffered
      setbuf( stream2, NULL ); // C4996
      printf( "stream2 buffering disabled\n" );
      _fcloseall();
   }
}
```

```Output
stream1 set to user-defined buffer at: 0012FCDC
stream2 buffering disabled
```

## <a name="see-also"></a>См. также раздел

[Потоковый ввод-вывод](../../c-runtime-library/stream-i-o.md)<br/>
[fclose, _fcloseall](fclose-fcloseall.md)<br/>
[fflush](fflush.md)<br/>
[fopen, _wfopen](fopen-wfopen.md)<br/>
[setvbuf](setvbuf.md)<br/>
