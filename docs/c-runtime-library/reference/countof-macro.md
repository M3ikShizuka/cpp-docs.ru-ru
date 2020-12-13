---
description: 'Дополнительные сведения о: _countof макросе'
title: Макрос _countof
ms.date: 03/22/2018
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
- _countof
- countof
helpviewer_keywords:
- countof macro
- _countof macro
ms.assetid: 86198767-f7e5-4beb-898d-3cbbf60350a3
ms.openlocfilehash: 190f47aa7bb6bcf6bbd9478cce9df90aca81b437
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97146462"
---
# <a name="_countof-macro"></a>Макрос _countof

Выполняет вычисление количества элементов в статическом массиве.

## <a name="syntax"></a>Синтаксис

```C
#define _countof(array) (sizeof(array) / sizeof(array[0]))
```

### <a name="parameters"></a>Параметры

*array*<br/>
Имя массива.

## <a name="return-value"></a>Возвращаемое значение

Количество элементов в массиве, выраженное в виде **size_t**.

## <a name="remarks"></a>Комментарии

**_countof** реализуется как макрос препроцессора, аналогичный функции. Версия C++ имеет дополнительный механизм шаблонов для обнаружения во время компиляции, если вместо статического объявленного массива передается указатель.

Убедитесь, что *массив* фактически является массивом, а не указателем. В языке C **_countof** выдает ошибочные результаты, если *массив* является указателем. В C++ **_countof** не удается скомпилировать, если *массив* является указателем.  Массив, переданный в качестве параметра функции *декайс в указатель*, что означает, что внутри функции нельзя использовать **_countof** для определения экстента массива.

## <a name="requirements"></a>Requirements (Требования)

|Макрос|Обязательный заголовок|
|-----------|---------------------|
|**_countof**|\<stdlib.h>|

## <a name="example"></a>Пример

```cpp
// crt_countof.cpp
#define _UNICODE
#include <stdio.h>
#include <stdlib.h>
#include <tchar.h>

int main( void )
{
   _TCHAR arr[20], *p;
   printf( "sizeof(arr) = %zu bytes\n", sizeof(arr) );
   printf( "_countof(arr) = %zu elements\n", _countof(arr) );
   // In C++, the following line would generate a compile-time error:
   // printf( "%zu\n", _countof(p) ); // error C2784 (because p is a pointer)

   _tcscpy_s( arr, _countof(arr), _T("a string") );
   // unlike sizeof, _countof works here for both narrow- and wide-character strings
}
```

```Output
sizeof(arr) = 40 bytes
_countof(arr) = 20 elements
```

## <a name="see-also"></a>См. также раздел

[Оператор sizeof](../../cpp/sizeof-operator.md)<br/>
