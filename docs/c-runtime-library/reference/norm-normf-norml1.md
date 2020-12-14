---
description: 'Дополнительные сведения: норма, нормф, норма'
title: norm, normf, norml
ms.date: 04/05/2018
api_name:
- norm
- normf
- norml
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
- norm
- normf
- norml
- complex/norm
- complex/normf
- complex/norml
helpviewer_keywords:
- norm function
- normf function
- norml function
ms.assetid: 9786ecfe-0019-4553-b378-0af6c691e15c
ms.openlocfilehash: 175cff5f9c0e31a56a86a96c3262e2c3c546fe4a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97256306"
---
# <a name="norm-normf-norml"></a>norm, normf, norml

Возвращает абсолютное значение комплексного числа в квадрате.

## <a name="syntax"></a>Синтаксис

```C
double norm( _Dcomplex z );
float normf( _Fcomplex z );
long double norml( _Lcomplex z );
```

```cpp
float norm( _Fcomplex z );  // C++ only
long double norm( _Lcomplex z );  // C++ only
```

### <a name="parameters"></a>Параметры

*з*<br/>
Комплексное число.

## <a name="return-value"></a>Возвращаемое значение

Величина квадрата *z*.

## <a name="remarks"></a>Комментарии

Поскольку C++ допускает перегрузку, можно вызывать перегрузки **нормы** , которые принимают **_Fcomplex** или **_Lcomplex** значения, а также возвращают **`float`** **`long double`** значения или. В программе на языке C **норма** всегда принимает значение **_Dcomplex** и возвращает **`double`** значение.

## <a name="requirements"></a>Требования

|Подпрограмма|Заголовок C|Заголовок C++|
|-------------|--------------|------------------|
|**норма**, **нормф**, **норма**|\<complex.h>|\<complex.h>|

Типы **_Fcomplex**, **_Dcomplex** и **_Lcomplex** являются эквивалентами корпорации Майкрософт нереализованных собственных типов C99 с **плавающей запятой _Complex**, **Double _Complex** и **long double _Complex** соответственно.  Дополнительные сведения о совместимости см. в разделе [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="see-also"></a>См. также раздел

[Алфавитный справочник по функциям](crt-alphabetical-function-reference.md)<br/>
[creal, crealf, creall](creal-crealf-creall.md)<br/>
[cproj, cprojf, cprojl](cproj-cprojf-cprojl.md)<br/>
[conj, conjf, conjl](conj-conjf-conjl.md)<br/>
[cimag, cimagf, cimagl](cimag-cimagf-cimagl.md)<br/>
[carg, cargf, cargl](carg-cargf-cargl.md)<br/>
[cabs, cabsf, cabsl](cabs-cabsf-cabsl.md)<br/>
