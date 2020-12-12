---
description: 'Дополнительные сведения: _CIsqrt'
title: _CIsqrt
ms.date: 4/2/2020
api_name:
- _CIsqrt
- _o__CIsqrt
api_location:
- msvcr90.dll
- msvcr80.dll
- msvcr110_clr0400.dll
- msvcr120.dll
- msvcrt.dll
- msvcr110.dll
- msvcr100.dll
- api-ms-win-crt-math-l1-1-0.dll
- api-ms-win-crt-private-l1-1-0.dll
api_type:
- DLLExport
topic_type:
- apiref
f1_keywords:
- _CIsqrt
- CIsqrt
helpviewer_keywords:
- CIsqrt intrinsic
- _CIsqrt intrinsic
ms.assetid: 663548ea-398c-48ee-8397-a787c6ebb937
ms.openlocfilehash: b643ad301acc217f3fac1bbf1aeee1d7141702a4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97209624"
---
# <a name="_cisqrt"></a>_CIsqrt

Вычисляет квадратный корень верхнего значения в стеке.

## <a name="syntax"></a>Синтаксис

```cpp
void __cdecl _CIsqrt();
```

## <a name="remarks"></a>Remarks

Эта версия функции `sqrt` включает специальные соглашения о вызовах, распознаваемые компилятором. Это ускоряет выполнение, поскольку исключает создание копий и помогает распределять регистры.

Полученное значение помещается в верхнюю часть стека.

По умолчанию глобальное состояние этой функции ограничивается приложением. Чтобы изменить это, см. раздел [глобальное состояние в CRT](global-state.md).

## <a name="requirements"></a>Требования

**Платформа:** x86

## <a name="see-also"></a>См. также раздел

[Алфавитный справочник по функциям](../c-runtime-library/reference/crt-alphabetical-function-reference.md)<br/>
[sqrt, sqrtf, sqrtl](../c-runtime-library/reference/sqrt-sqrtf-sqrtl.md)
