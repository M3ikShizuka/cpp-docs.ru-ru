---
description: 'Дополнительные сведения: _fpclass, _fpclassf'
title: _fpclass, _fpclassf
ms.date: 1/15/2021
api_name:
- _fpclass
- _fpclassf
- _o__fpclass
- _o__fpclassf
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
- fpclass
- _fpclass
- _fpclassf
- math/_fpclass
- float/_fpclass
- math/_fpclassf
helpviewer_keywords:
- fpclass function
- floating-point numbers, IEEE representation
- _fpclass function
- _fpclassf function
ms.openlocfilehash: 3fb97c5aa787c4c102e787fa3b08650f23ca546a
ms.sourcegitcommit: 92dc6d99ba5dcf3b64dee164df2d29beb1e608da
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/18/2021
ms.locfileid: "98563995"
---
# <a name="_fpclass-_fpclassf"></a>`_fpclass`, `_fpclassf`

Возвращает значение, указывающее классификацию числа с плавающей запятой для аргумента.

## <a name="syntax"></a>Синтаксис

```C
int _fpclass(
   double x
);

int _fpclassf(
   float x
); /* x64 only */
```

### <a name="parameters"></a>Параметры

*`x`*\
Проверяемое значение с плавающей запятой.

## <a name="return-value"></a>Возвращаемое значение

**`_fpclass`** Функции и **`_fpclassf`** возвращают целочисленное значение, которое указывает на классификацию с плавающей запятой аргумента *`x`* . Классификация может иметь одно из следующих значений, определенных в `<float.h>` .

|Значение|Описание|
|-----------|-----------------|
|**`_FPCLASS_SNAN`**|Сигнальное значение NaN|
|**`_FPCLASS_QNAN`**|Несигнальное значение NaN|
|**`_FPCLASS_NINF`**|Отрицательная бесконечность ( `-INF` )|
|**`_FPCLASS_NN`**|Отрицательное ненулевое нормализованное значение|
|**`_FPCLASS_ND`**|Отрицательное денормализованное значение|
|**`_FPCLASS_NZ`**|Отрицательный ноль (-0)|
|**`_FPCLASS_PZ`**|Положительный 0 (+ 0)|
|**`_FPCLASS_PD`**|Положительное денормализованное значение|
|**`_FPCLASS_PN`**|Положительное ненулевое нормализованное значение|
|**`_FPCLASS_PINF`**|Положительная бесконечность ( `+INF` )|

## <a name="remarks"></a>Комментарии

**`_fpclass`** Функции и **`_fpclassf`** являются специфичными для Microsoft. Они похожи на [`fpclassify`](fpclassify.md) , но возвращают более подробные сведения об аргументе. **`_fpclassf`** Функция доступна только при компиляции для платформы x64.

По умолчанию глобальное состояние этой функции ограничивается приложением. Чтобы изменить это, см. раздел [глобальное состояние в CRT](../global-state.md).

## <a name="requirements"></a>Требования

|Функция|Обязательный заголовок|
|--------------|---------------------|
|**`_fpclass`**, **`_fpclassf`**|`<float.h>`|

Дополнительные сведения о совместимости см. в разделе [Совместимость](../../c-runtime-library/compatibility.md).

## <a name="see-also"></a>См. также

[Поддержка операций с плавающей запятой](../../c-runtime-library/floating-point-support.md)\
[`isnan`, `_isnan`, `_isnanf`](isnan-isnan-isnanf.md)\
[`fpclassify`](fpclassify.md)