---
description: 'Дополнительные сведения: _Cmulcc, _FCmulcc, _LCmulcc'
title: _Cmulcc, _FCmulcc, _LCmulcc
ms.date: 03/30/2018
api_name:
- _Cmulcc
- _FCmulcc
- _LCmulcc
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
- _Cmulcc
- _FCmulcc
- _LCmulcc
- complex/_Cmulcc
- complex/_FCmulcc
- complex/_LCmulcc
helpviewer_keywords:
- _Cmulcc function
- _FCmulcc function
- _LCmulcc function
ms.openlocfilehash: e18f6ee0ab166cbce04d425ece43ef8ba2708a4c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97258737"
---
# <a name="_cmulcc-_fcmulcc-_lcmulcc"></a>_Cmulcc, _FCmulcc, _LCmulcc

Умножает два комплексных числа.

## <a name="syntax"></a>Синтаксис

```C
_Dcomplex _Cmulcc( _Dcomplex x, _Dcomplex y );
_Fcomplex _FCmulcc( _Fcomplex x, _Fcomplex y );
_Lcomplex _LCmulcc( _Lcomplex x, _Lcomplex y );
```

### <a name="parameters"></a>Параметры

*x*<br/>
Один из сложных операндов для умножения.

*y*<br/>
Другой сложный операнд для умножения.

## <a name="return-value"></a>Возвращаемое значение

Структура **_Dcomplex**, **_Fcomplex** или **_Lcomplex** , представляющая комплексное произведение комплексных чисел *x* и *y*.

## <a name="remarks"></a>Комментарии

Поскольку встроенные арифметические операторы не работают в реализации сложных типов Майкрософт, функции **_Cmulcc**, **_FCmulcc** и **_LCmulcc** упрощают умножение сложных типов.

## <a name="requirements"></a>Требования

|Подпрограмма|Заголовок C|Заголовок C++|
|-------------|--------------|------------------|
|**_Cmulcc**, **_FCmulcc** **_LCmulcc**|\<complex.h>|\<complex.h>|

Эти функции относятся только к Microsoft. Типы **_Dcomplex**, **_Fcomplex** и **_Lcomplex** являются эквивалентами, специфичными для Microsoft, для нереализованных C99 машинных типов **Double _Complex**, **float _Complex** и **long double _Complex** соответственно. Дополнительные сведения о совместимости см. в разделе [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="see-also"></a>См. также раздел

[Алфавитный справочник по функциям](crt-alphabetical-function-reference.md)<br/>
[_Cbuild, _FCbuild, _LCbuild](cbuild-fcbuild-lcbuild.md)<br/>
[_Cmulcr, _FCmulcr, _LCmulcr](cmulcr-fcmulcr-lcmulcr.md)<br/>
[norm, normf, norml](norm-normf-norml1.md)<br/>
[cproj, cprojf, cprojl](cproj-cprojf-cprojl.md)<br/>
[conj, conjf, conjl](conj-conjf-conjl.md)<br/>
[creal, crealf, creall](creal-crealf-creall.md)<br/>
[cimag, cimagf, cimagl](cimag-cimagf-cimagl.md)<br/>
[carg, cargf, cargl](carg-cargf-cargl.md)<br/>
[cabs, cabsf, cabsl](cabs-cabsf-cabsl.md)<br/>
