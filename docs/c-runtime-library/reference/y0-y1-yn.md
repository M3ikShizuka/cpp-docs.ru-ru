---
description: 'Дополнительные сведения о: Y0, y1, yn'
title: y0, y1, yn
ms.date: 12/16/2019
api_name:
- y1
- yn
- y0
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
- DLLExport
topic_type:
- apiref
f1_keywords:
- yn
- y1
- y0
helpviewer_keywords:
- y0 function
- y1 function
- yn function
ms.assetid: e14215f3-53d4-4ae8-816e-4c1ec2019316
ms.openlocfilehash: d59ea472509f0eba050da12f8867f48d25cb1f63
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97309109"
---
# <a name="y0-y1-yn"></a>y0, y1, yn

Имена функций POSIX `y0` , `y1` , и `yn` являются устаревшими псевдонимами для функций [_y0, _y1 и _yn](bessel-functions-j0-j1-jn-y0-y1-yn.md) . По умолчанию они генерируют [Предупреждение компилятора (уровень 3) C4996](../../error-messages/compiler-warnings/compiler-warning-level-3-c4996.md). Имена являются устаревшими, так как они не соответствуют стандартным правилам C для имен, зависящих от реализации. Однако функции по-прежнему поддерживаются.

Вместо этого рекомендуется использовать [_y0, _y1 и _yn](bessel-functions-j0-j1-jn-y0-y1-yn.md) . Вы также можете продолжать использовать эти имена функций и отключить предупреждение. Дополнительные сведения см. [в разделе Отключение](../../error-messages/compiler-warnings/compiler-warning-level-3-c4996.md#turn-off-the-warning) [имен функций](../../error-messages/compiler-warnings/compiler-warning-level-3-c4996.md#posix-function-names)Warning и POSIX.
