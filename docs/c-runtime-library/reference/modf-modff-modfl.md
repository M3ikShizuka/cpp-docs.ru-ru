---
title: modf, modff, modfl
description: Справочник по API для modf, modff и модфл; который разбивает значение с плавающей запятой на части дробной и целой частей.
ms.date: 1/15/2021
api_name:
- modff
- modf
- modfl
- _o_modf
- _o_modff
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
- modff
- _modfl
- modf
- modfl
- math/modf
- math/modff
- math/modfl
helpviewer_keywords:
- modf function
- modff function
- modfl function
ms.openlocfilehash: fbc68c3369e8b992350534e3baa5f19b0f2a5e39
ms.sourcegitcommit: 92dc6d99ba5dcf3b64dee164df2d29beb1e608da
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/18/2021
ms.locfileid: "98564022"
---
# <a name="modf-modff-modfl"></a>`modf`, `modff`, `modfl`

Разбивает значение с плавающей запятой на дробную и целую части.

## <a name="syntax"></a>Синтаксис

```C
double modf( double x, double * intptr );
float modff( float x, float * intptr );
long double modfl( long double x, long double * intptr );
```

```cpp
float modf( float x, float * intptr );  // C++ only
long double modf( long double x, long double * intptr );  // C++ only
```

### <a name="parameters"></a>Параметры

*`x`*\
Значение с плавающей запятой.

*`intptr`*\
Указатель на сохраненное значение целой части числа.

## <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает знак дробной части *`x`* . Ошибки не возвращаются.

## <a name="remarks"></a>Комментарии

Функции **modf** разбивают значение с плавающей запятой *`x`* на дробные и целые части, каждый из которых имеет тот же знак, что и *`x`* . Возвращается дробная часть со знаком в *`x`* . Целая часть хранится в виде значения с плавающей запятой в *`intptr`* .

**modf** имеет реализацию, использующую Streaming SIMD Extensions 2 (SSE2). [`_set_SSE2_enable`](set-sse2-enable.md)Сведения и ограничения по использованию реализации SSE2 см. в разделе.

C++ допускает перегрузку, поэтому можно вызывать перегрузки **`modf`** , которые принимают и возвращают **`float`** **`long double`** Параметры или. В программе на языке C **`modf`** всегда принимает два значения типа Double и возвращает значение типа Double.

По умолчанию глобальное состояние этой функции ограничивается приложением. Чтобы изменить это, см. раздел [глобальное состояние в CRT](../global-state.md).

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|**`modf`**, **`modff`**, **`modfl`**|Ц `<math.h>`<br /><br /> C++: `<cmath>` или `<math.h>`|

Дополнительные сведения о совместимости см. в разделе [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="example"></a>Пример

```C
// crt_modf.c

#include <math.h>
#include <stdio.h>

int main( void )
{
   double x, y, n;

   x = -14.87654321;      /* Divide x into its fractional */
   y = modf( x, &n );     /* and integer parts            */

   printf( "For %f, the fraction is %f and the integer is %.f\n",
           x, y, n );
}
```

```Output
For -14.876543, the fraction is -0.876543 and the integer is -14
```

## <a name="see-also"></a>См. также

[Поддержка операций с плавающей запятой](../../c-runtime-library/floating-point-support.md)\
[`frexp`](frexp.md)\
[`ldexp`](ldexp.md)