---
description: 'Дополнительные сведения о: fpclassify'
title: fpclassify
ms.date: 04/05/2018
api_name:
- fpclassify
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
- HeaderDef
f1_keywords:
- fpclassify
- math/fpclassify
helpviewer_keywords:
- fpclassify macro
- fpclassify function
ms.assetid: bf549499-7ff9-4a58-8692-f2d1cb6bab81
ms.openlocfilehash: 716684f15e82fb439c16239a61401b892a244f93
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97164839"
---
# <a name="fpclassify"></a>fpclassify

Возвращает значение, указывающее классификацию числа с плавающей запятой для аргумента.

## <a name="syntax"></a>Синтаксис

```C
int fpclassify(
   /* floating-point */ x
);

int fpclassify(
   float x
); // C++ only

int fpclassify(
   double x
); // C++ only

int fpclassify(
   long double x
); // C++ only
```

### <a name="parameters"></a>Параметры

*x*<br/>
Проверяемое значение с плавающей запятой.

## <a name="return-value"></a>Возвращаемое значение

**fpclassify** возвращает целочисленное значение, указывающее класс с плавающей запятой аргумента *x*. В этой таблице показаны возможные значения, возвращаемые функцией **fpclassify**, определенной в \<math.h> .

|Значение|Описание|
|-----------|-----------------|
|**FP_NAN**|Сигнальное, несигнальное или неопределенное значение NaN|
|**FP_INFINITE**|Положительная или отрицательная бесконечность|
|**FP_NORMAL**|Положительное или отрицательное нормализованное ненулевое значение|
|**FP_SUBNORMAL**|Положительное или отрицательное денормализованное значение|
|**FP_ZERO**|Положительное или отрицательное нулевое значение|

## <a name="remarks"></a>Комментарии

В языке C **fpclassify** является макросом; в C++ **fpclassify** — это функция, перегруженная с помощью типов аргументов **`float`** , **`double`** или **`long double`** . В обоих случаях возвращаемое значение зависит от действительного типа выражения аргумента, а не от промежуточного представления. Например, обычная **`double`** или **`long double`** значение может стать бесконечным, нормальным или нулевым значением при преобразовании в **`float`** .

## <a name="requirements"></a>Требования

|Функция или макрос|Обязательный заголовок (C)|Обязательный заголовок (C++)|
|---------------------|---------------------------|-------------------------------|
|**fpclassify**|\<math.h>|\<math.h> или \<cmath>|

Макросы **fpclassify** и функции **fpclassify** соответствуют спецификациям ISO C99 и c++ 11. Дополнительные сведения о совместимости см. в разделе [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="see-also"></a>См. также раздел

[Поддержка операций с плавающей запятой](../../c-runtime-library/floating-point-support.md)<br/>
[isnan, _isnan, _isnanf](isnan-isnan-isnanf.md)<br/>
