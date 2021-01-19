---
title: cosh, coshf, coshl
description: Справочник по API для cosh, кошф и кошл; который вычисляет гиперболический косинус значения с плавающей запятой.
ms.date: 1/15/2021
api_name:
- cosh
- coshf
- coshl
- _o_cosh
- _o_coshf
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
- api-ms-win-crt-private-l1-1-0.dll
api_type:
- DLLExport
topic_type:
- apiref
f1_keywords:
- cosh
- coshf
- coshl
helpviewer_keywords:
- cosh function
- coshf function
- coshl function
- trigonometric functions
- hyperbolic functions
ms.openlocfilehash: c010dcdc30b16f94f55fca99d67b58e5c19370c7
ms.sourcegitcommit: 92dc6d99ba5dcf3b64dee164df2d29beb1e608da
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/18/2021
ms.locfileid: "98564099"
---
# <a name="cosh-coshf-coshl"></a>`cosh`, `coshf`, `coshl`

Вычисляет гиперболический косинус.

## <a name="syntax"></a>Синтаксис

```C
double cosh( double x );
float coshf( float x );
long double coshl( long double x );
#define cosh(X) // Requires C11 or higher

float cosh( float x );  // C++ only
long double cosh( long double x );  // C++ only
```

### <a name="parameters"></a>Параметры

*`x`*\
Угол в радианах.

## <a name="return-value"></a>Возвращаемое значение

Гиперболический косинус *`x`* .

По умолчанию, если результат слишком велик в **`cosh`** **`coshf`** **`coshl`** методе, или, функция возвращает **`HUGE_VAL`** и устанавливает **`errno`** для значение **`ERANGE`** .

|Входные данные|Исключение SEH|`Matherr` об|
|-----------|-------------------|-----------------------|
|± **`QNAN`**, **`IND`**|нет|**`_DOMAIN`**|
|*`x`* ≥ 7.104760 e + 002|**`INEXACT`**+**`OVERFLOW`**|**`OVERFLOW`**|

## <a name="remarks"></a>Комментарии

Поскольку C++ допускает перегрузку, можно вызывать перегрузки **`cosh`** , которые принимают и возвращают **`float`** **`long double`** значения или. В программе на языке C, если только вы не используете `<tgmath.h>` макрос для вызова этой функции, **`cosh`** всегда принимает и возвращает **`double`** .

При использовании `<tgmath.h>` `cosh()` макроса тип аргумента определяет, какая версия функции выбрана. Подробные сведения см. в разделе [Type-Generic Math](../../c-runtime-library/tgmath.md) .

По умолчанию глобальное состояние этой функции ограничивается приложением. Чтобы изменить это, см. раздел [глобальное состояние в CRT](../global-state.md).

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок (C)|Обязательный заголовок (C++)|
|-------------|---------------------|-|
|**`coshf`**, **`cosl`**, **`coshl`**|`<math.h>`|`<cmath>` или `<math.h>`|
|**`coshf()`** макровирусах | `<tgmath.h>` ||

Дополнительные сведения о совместимости см. в разделе [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="example"></a>Пример

См. пример в [ `sinh` , `sinhf` , `sinhl` ](sinh-sinhf-sinhl.md).

## <a name="see-also"></a>См. также

[Поддержка операций с плавающей запятой](../../c-runtime-library/floating-point-support.md)\
[`acosh, acoshf, acoshl`](acosh-acoshf-acoshl.md)\
[`asinh, asinhf, asinhl`](asinh-asinhf-asinhl.md)\
[`atanh, atanhf, atanhl`](atanh-atanhf-atanhl.md)\
[`_matherr`](matherr.md)\
[`sinh, sinhf, sinhl`](sinh-sinhf-sinhl.md)\
[`tanh, tanhf, tanhl`](tanh-tanhf-tanhl.md)