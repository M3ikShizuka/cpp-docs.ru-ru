---
description: 'Дополнительные сведения о: clog10, clog10f, clog10l'
title: clog10, clog10f, clog10l
ms.date: 11/04/2016
api_name:
- clog10
- clog10f
- clog10l
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
- api-ms-win-crt-math-l1-1-0.dll
api_type:
- DLLExport
topic_type:
- apiref
f1_keywords:
- clog10
- clog10f
- clog10l
- complex/clog10
- complex/clog10f
- complex/clog10l
helpviewer_keywords:
- clog10 function
- clog10f function
- clog10l function
ms.assetid: 2ddae00d-ef93-4441-add3-f4d58358401b
ms.openlocfilehash: 8f3112cec5d7f0d75435c1f47c8a28c9d3c93d69
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97277249"
---
# <a name="clog10-clog10f-clog10l"></a>clog10, clog10f, clog10l

Извлекает десятичный логарифм комплексного числа.

## <a name="syntax"></a>Синтаксис

```C
_Dcomplex clog10( _Dcomplex z );
_Fcomplex clog10f( _Fcomplex z );
_Lcomplex clog10l( _Lcomplex z );
```

```cpp
_Fcomplex clog10( _Fcomplex z );  // C++ only
_Lcomplex clog10( _Lcomplex z );  // C++ only
```

### <a name="parameters"></a>Параметры

*з*<br/>
Основание логарифма.

## <a name="return-value"></a>Возвращаемое значение

Возможны следующие возвращаемые значения:

|параметр z|Возвращаемое значение|
|-----------------|------------------|
|Положительное число|Десятичный логарифм z|
|Нуль|- ∞|
|Отрицательное число|Не число|
|Не число|Не число|
|+ ∞|+ ∞|

## <a name="remarks"></a>Комментарии

Поскольку C++ допускает перегрузку, можно вызывать перегрузки **clog10** , которые принимают и возвращают **_Fcomplex** и **_Lcomplex** значения. В программе на языке C **clog10** всегда принимает и возвращает значение **_Dcomplex** .

## <a name="requirements"></a>Требования

|Подпрограмма|Заголовок C|Заголовок C++|
|-------------|--------------|------------------|
|**clog10**,               **clog10f**, **клогл**|\<complex.h>|\<ccomplex>|

Дополнительные сведения о совместимости см. в разделе [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="see-also"></a>См. также раздел

[Алфавитный справочник по функциям](crt-alphabetical-function-reference.md)<br/>
[cexp, cexpf, cexpl](cexp-cexpf-cexpl.md)<br/>
[cpow, cpowf, cpowl](cpow-cpowf-cpowl.md)<br/>
[clog, clogf, clogl](clog-clogf-clogl.md)<br/>
