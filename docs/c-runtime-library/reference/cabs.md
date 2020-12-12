---
description: 'Дополнительные сведения: _cabs'
title: _cabs
ms.date: 4/2/2020
api_name:
- _cabs
- _o__cabs
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
- _cabs
helpviewer_keywords:
- cabs function
- absolute values
- _cabs function
- calculating absolute values
ms.assetid: fea292ee-1a39-4a0a-b416-4a189346ff26
ms.openlocfilehash: 362121ab160e46ec0922b193ccedf77d5bf99468
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97171638"
---
# <a name="_cabs"></a>_cabs

Вычисляет абсолютное значение комплексного числа.

## <a name="syntax"></a>Синтаксис

```C
double _cabs(
   struct _complex z
);
```

### <a name="parameters"></a>Параметры

*з*<br/>
Комплексное число.

## <a name="return-value"></a>Возвращаемое значение

При успешном выполнении **_cabs** возвращает абсолютное значение его аргумента. При переполнении **_cabs** возвращает **HUGE_VAL** **и задает для** **ERANGE**. Изменить обработку ошибок можно с помощью функции [_matherr](matherr.md).

## <a name="remarks"></a>Комментарии

Функция **_cabs** вычисляет абсолютное значение комплексного числа, которое должно быть структурой типа [_complex](../../c-runtime-library/standard-types.md). Структура *z* состоит из вещественного компонента *x* и мнимого компонента *y*. Вызов **_cabs** возвращает значение, эквивалентное значению выражения `sqrt( z.x * z.x + z.y * z.y )` .

По умолчанию глобальное состояние этой функции ограничивается приложением. Чтобы изменить это, см. раздел [глобальное состояние в CRT](../global-state.md).

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|**_cabs**|\<math.h>|

Дополнительные сведения о совместимости см. в разделе [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="example"></a>Пример

```C
// crt_cabs.c
// Using _cabs, this program calculates
// the absolute value of a complex number.

#include <math.h>
#include <stdio.h>

int main( void )
{
   struct _complex number = { 3.0, 4.0 };
   double d;

   d = _cabs( number );
   printf( "The absolute value of %f + %fi is %f\n",
           number.x, number.y, d );
}
```

```Output
The absolute value of 3.000000 + 4.000000i is 5.000000
```

## <a name="see-also"></a>См. также раздел

[Поддержка операций с плавающей запятой](../../c-runtime-library/floating-point-support.md)<br/>
[abs, labs, llabs, _abs64](abs-labs-llabs-abs64.md)<br/>
[fabs, fabsf, fabsl](fabs-fabsf-fabsl.md)
