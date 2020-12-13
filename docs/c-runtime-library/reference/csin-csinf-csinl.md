---
description: 'Дополнительные сведения о: Ксин, ксинф, ксинл'
title: csin, csinf, csinl
ms.date: 11/04/2016
api_name:
- csin
- csinf
- csinl
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
- csin
- csinf
- csinl
- complex/csin
- complex/csinf
- complex/csinl
helpviewer_keywords:
- csin function
- csinf function
- csinl function
ms.assetid: 3ed475e8-9aae-42ba-a25c-7ae656a0fd4d
ms.openlocfilehash: d19f916f6fdd9e871eef6e1ad77369642b939495
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97178866"
---
# <a name="csin-csinf-csinl"></a>csin, csinf, csinl

Извлекают синус комплексного числа.

## <a name="syntax"></a>Синтаксис

```C
_Dcomplex csin(
   _Dcomplex z
);
_Fcomplex csin(
   _Fcomplex z
);  // C++ only
_Lcomplex csin(
   _Lcomplex z
);  // C++ only
_Fcomplex csinf(
   _Fcomplex z
);
_Lcomplex csinl(
   _Lcomplex z
);
```

### <a name="parameters"></a>Параметры

*з*<br/>
Комплексное число, указывающее угол в радианах.

## <a name="return-value"></a>Возвращаемое значение

Синус *z* в радианах.

## <a name="remarks"></a>Комментарии

Поскольку C++ допускает перегрузку, можно вызывать перегрузки **Ксин** , которые принимают и возвращают **_Fcomplex** и **_Lcomplex** значения. В программе на языке C **Ксин** всегда принимает и возвращает значение **_Dcomplex** .

## <a name="requirements"></a>Требования

|Подпрограмма|Заголовок C|Заголовок C++|
|-------------|--------------|------------------|
|**Ксин**,               **ксинф**, **ксинл**|\<complex.h>|\<ccomplex>|

Дополнительные сведения о совместимости см. в разделе [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="see-also"></a>См. также раздел

[Алфавитный справочник по функциям](crt-alphabetical-function-reference.md)<br/>
[catanh, catanhf, catanhl](catanh-catanhf-catanhl.md)<br/>
[ctanh, ctanhf, ctanhl](ctanh-ctanhf-ctanhl.md)<br/>
[catan, catanf, catanl](catan-catanf-catanl.md)<br/>
[csinh, csinhf, csinhl](csinh-csinhf-csinhl.md)<br/>
[casinh, casinhf, casinhl](casinh-casinhf-casinhl.md)<br/>
[ccosh, ccoshf, ccoshl](ccosh-ccoshf-ccoshl.md)<br/>
[cacosh, cacoshf, cacoshl](cacosh-cacoshf-cacoshl.md)<br/>
[cacos, cacosf, cacosl](cacos-cacosf-cacosl.md)<br/>
[ctan, ctanf, ctanl](ctan-ctanf-ctanl.md)<br/>
[casin, casinf, casinl](casin-casinf-casinl.md)<br/>
[ccos, ccosf, ccosl](ccos-ccosf-ccosl.md)<br/>
[csqrt, csqrtf, csqrtl](csqrt-csqrtf-csqrtl.md)<br/>
