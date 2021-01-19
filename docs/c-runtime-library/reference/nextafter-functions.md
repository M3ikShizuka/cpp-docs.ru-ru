---
title: nextafter, nextafterf, nextafterl, _nextafter, _nextafterf, nexttoward, nexttowardf, nexttowardl
description: Справочник по API для nextafter, некстафтерф, некстафтерл, _nextafter, _nextafterf, нексттовард, нексттовардф и нексттовардл; который возвращает следующее представимое значение с плавающей точкой.
ms.date: 1/15/2021
api_name:
- nextafterf
- _nextafterf
- nextafter
- nextafterl
- _nextafter
- nexttoward
- nexttowardf
- nexttowardl
- _o__nextafter
- _o_nextafter
- _o_nextafterf
- _o_nextafterl
- _o_nexttoward
- _o_nexttowardf
- _o_nexttowardl
- _o__nextafterf
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
- nextafter
- _nextafter
- nextafterf
- nextafterl
- _nextafterf
- math/nextafter
- math/nextafterf
- math/nextafterl
- nexttoward
- nexttowardf
- nexttowardl
- math/nexttoward
- math/nexttowardf
- math/nexttowardl
helpviewer_keywords:
- _nextafter function
- nextafter function
- _nextafterf function
- nextafterf function
- nextafterl function
- nexttoward function
- nexttowardf function
- nexttowardl function
ms.openlocfilehash: 664ddb204fa089f83acebf6a9042b17a776ea306
ms.sourcegitcommit: 92dc6d99ba5dcf3b64dee164df2d29beb1e608da
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/18/2021
ms.locfileid: "98564138"
---
# <a name="nextafter-nextafterf-nextafterl-_nextafter-_nextafterf-nexttoward-nexttowardf-nexttowardl"></a>`nextafter`, `nextafterf`, `nextafterl`, `_nextafter`, `_nextafterf`, `nexttoward`, `nexttowardf`, `nexttowardl`

Возвращает следующее представимое значение с плавающей запятой.

## <a name="syntax"></a>Синтаксис

```C
double nextafter( double x, double y );
float nextafterf( float x, float y );
long double nextafterl( long double x, long double y );

double _nextafter( double x, double y );
float _nextafterf( float x, float y ); /* x64 only */

#define nextafter(X, Y) // Requires C11 or higher

double nexttoward( double x, long double y );
float nexttowardf( float x, long double y );
long double nexttowardl( long double x, long double y );

#define nexttoward(X, Y) // Requires C11 or higher

float nextafter( float x, float y ); /* C++ only, requires <cmath> */
long double nextafter( long double x, long double y ); /* C++ only, requires <cmath> */

float nexttoward( float x, long double y ); /* C++ only, requires <cmath> */
long double nexttoward( long double x, long double y ); /* C++ only, requires <cmath> */
```

### <a name="parameters"></a>Параметры

*`x`*\
Начальное значение с плавающей запятой.

*`y`*\
Следующее значение с плавающей запятой.

## <a name="return-value"></a>Возвращаемое значение

Возвращает следующее представимое значение с плавающей запятой возвращаемого типа после *`x`* в направлении *`y`* . Если *`x`* и *`y`* равны, функция возвращает *`y`* , преобразованную в тип возвращаемого значения без исключения. Если значение *`x`* не равно *`y`* , а результат является нормальным или нулем, то **`FE_UNDERFLOW`** **`FE_INEXACT`** задаются состояния исключения и, а также возвращается правильный результат. Если параметр *`x`* или *`y`* является NaN, то возвращаемое значение является одним из входных значений NaN. Если *`x`* Конечная точка является конечной, а результат является бесконечным или не может быть представлен в типе, возвращается правильно подписанная бесконечность или NaN, **`FE_OVERFLOW`** а также **`FE_INEXACT`** состояния исключений с плавающей запятой и устанавливаются **`errno`** в значение **`ERANGE`** .

## <a name="remarks"></a>Комментарии

**`nextafter`** **`nexttoward`** Семейства функций и эквивалентны, за исключением типа параметра *`y`* . Если *`x`* и *`y`* равны, возвращаемое значение *`y`* преобразуется в тип возвращаемого значения.

Поскольку C++ допускает перегрузку, при включении `<cmath>` можно вызывать перегрузки **`nextafter`** и **`nexttoward`** , которые возвращают **`float`** **`long double`** типы и. В программе на языке C, если только вы не используете `<tgmath.h>` макрос для вызова этой функции **`nextafter`** и **`nexttoward`** всегда возвращает **`double`** .

При использовании `<tgmath.h>` `nextafter()` `nexttoward()` макроса или тип аргумента определяет, какая версия функции выбрана. Подробные сведения см. в разделе [Type-Generic Math](../../c-runtime-library/tgmath.md) .

Функции **_nextafter** и **_nextafterf** являются специфичными для Microsoft. Функция **_nextafterf** доступна только при компиляции для x64.

По умолчанию глобальное состояние этой функции ограничивается приложением. Чтобы изменить это, см. раздел [глобальное состояние в CRT](../global-state.md).

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок (C)|Обязательный заголовок (C++)|
|-------------|---------------------------|-------------------------------|
|**`nextafter`**, **`nextafterf`**, **`nextafterl`**, **`_nextafterf`**, **`nexttoward`**, **`nexttowardf`**, **`nexttowardl`**|`<math.h>`|`<math.h>` или `<cmath>`|
|**`_nextafter`**|`<float.h>`|`<float.h>` или `<cfloat>`|
|**`nextafter`** макрос,  **`nexttoward`** макрос| `<tgmath.h>` ||

Дополнительные сведения о совместимости см. в разделе [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="see-also"></a>См. также

[Поддержка операций с плавающей запятой](../../c-runtime-library/floating-point-support.md)\
[`isnan`, `_isnan`, `_isnanf`](isnan-isnan-isnanf.md)
