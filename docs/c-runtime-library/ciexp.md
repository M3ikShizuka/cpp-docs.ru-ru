---
description: 'Дополнительные сведения: _CIexp'
title: _CIexp
ms.date: 4/2/2020
api_name:
- _CIexp
- _o__CIexp
api_location:
- msvcr120.dll
- msvcr80.dll
- msvcr110.dll
- msvcr100.dll
- msvcrt.dll
- msvcr110_clr0400.dll
- msvcr90.dll
- api-ms-win-crt-math-l1-1-0.dll
- api-ms-win-crt-private-l1-1-0.dll
api_type:
- DLLExport
topic_type:
- apiref
f1_keywords:
- CIexp
- _CIexp
helpviewer_keywords:
- CIexp intrinsic
- _CIexp intrinsic
ms.assetid: f8a3e3b7-fa57-41a3-9983-6c81914cbb55
ms.openlocfilehash: bc1e4ccb081fe31f786fcd19d3d8c761a7472212
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97209676"
---
# <a name="_ciexp"></a>_CIexp

Вычисляет экспоненту верхнего значения в стеке.

## <a name="syntax"></a>Синтаксис

```cpp
void __cdecl _CIexp();
```

## <a name="remarks"></a>Remarks

Эта версия функции `exp` включает специальные соглашения о вызовах, распознаваемые компилятором. Это ускоряет выполнение, поскольку исключает создание копий и помогает распределять регистры.

Полученное значение помещается в верхнюю часть стека.

По умолчанию глобальное состояние этой функции ограничивается приложением. Чтобы изменить это, см. раздел [глобальное состояние в CRT](global-state.md).

## <a name="requirements"></a>Требования

**Платформа:** x86

## <a name="see-also"></a>См. также раздел

[Алфавитный справочник по функциям](../c-runtime-library/reference/crt-alphabetical-function-reference.md)<br/>
[exp, expf, expl](../c-runtime-library/reference/exp-expf.md)
