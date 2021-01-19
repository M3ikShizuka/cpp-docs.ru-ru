---
title: fabs, fabsf, fabsl
description: Справочник по API для Fabs, fabsf и фабсл; , который вычисляет абсолютное значение значения с плавающей запятой.
ms.date: 1/15/2021
api_name:
- fabsf
- fabs
- fabsl
- _o_fabs
- _o_fabsf
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
- fabs
- fabsf
- fabsl
- "math\fabs"
- "math\fabsf"
- "math\fabsl"
helpviewer_keywords:
- absolute values
- fabsf function
- calculating absolute values
- fabs function
- fabsl function
ms.openlocfilehash: 453965b846dff9affb3fa6dce99ea8b6189a5d6c
ms.sourcegitcommit: 92dc6d99ba5dcf3b64dee164df2d29beb1e608da
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/18/2021
ms.locfileid: "98563930"
---
# <a name="fabs-fabsf-fabsl"></a>`fabs`, `fabsf`, `fabsl`

Вычисляет абсолютное значение аргумента с плавающей точкой.

## <a name="syntax"></a>Синтаксис

```C
double fabs(
   double x
);
float fabs(
   float x
); // C++ only
long double fabs(
   long double x
); // C++ only
float fabsf(
   float x
);
long double fabsl(
   long double x
);

#define fabs(X) // Requires C11 or higher
```

### <a name="parameters"></a>Параметры

*`x`*\
Значение с плавающей запятой.

## <a name="return-value"></a>Возвращаемое значение

**`fabs`** Функции возвращают абсолютное значение аргумента *x*. Ошибки не возвращаются.

|Входные данные|Исключение SEH|`Matherr` об|
|-----------|-------------------|-----------------------|
|± `QNAN`,`IND`|нет|`_DOMAIN`|

## <a name="remarks"></a>Комментарии

C++ допускает перегрузку, поэтому можно вызывать перегрузки **`fabs`** при включении `<cmath>` заголовка. В программе на языке C, если только вы не используете `<tgmath.h>` макрос для вызова этой функции, **`fabs`** всегда принимает и возвращает **`double`** .

При использовании `<tgmath.h>` `fabs()` макроса тип аргумента определяет, какая версия функции выбрана. Подробные сведения см. в разделе [Type-Generic Math](../../c-runtime-library/tgmath.md) .

По умолчанию глобальное состояние этой функции ограничивается приложением. Чтобы изменить это, см. раздел [глобальное состояние в CRT](../global-state.md).

## <a name="requirements"></a>Требования

|Функция|Обязательный заголовок C|Обязательный заголовок C++|
|--------------|-----------------------|---------------------------|
|**`fabs`**, **`fabsf`**, **`fabsl`**|`<math.h>`|`<cmath>` или `<math.h>`|
|**`fabs`** макровирусах | `<tgmath.h>` ||

Дополнительные сведения о совместимости см. в разделе [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="example"></a>Пример

См. пример для [`abs`](abs-labs-llabs-abs64.md) .

## <a name="see-also"></a>См. также

[Поддержка операций с плавающей запятой](../../c-runtime-library/floating-point-support.md)\
[`abs, labs, llabs, _abs64`](abs-labs-llabs-abs64.md)\
[`_cabs`](cabs.md)
