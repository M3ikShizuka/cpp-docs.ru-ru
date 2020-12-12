---
description: 'Дополнительные сведения о: струпр, вксупр'
title: strupr, wcsupr
ms.date: 12/16/2019
api_name:
- strupr
- wcsupr
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
- strupr
- wcsupr
helpviewer_keywords:
- strupr function
- wcsupr function
ms.assetid: 17dfe1cd-3b09-4702-9f89-2207f44953e6
ms.openlocfilehash: aefd25cc4d2a8d3fa51fba2da323c74ed199d116
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97326285"
---
# <a name="strupr-wcsupr"></a>strupr, wcsupr

Имена функций, специфичных для Microsoft, `strupr` и `wcsupr` являются устаревшими псевдонимами для функций [_strupr и _wcsupr](strupr-strupr-l-mbsupr-mbsupr-l-wcsupr-l-wcsupr.md) . По умолчанию они генерируют [Предупреждение компилятора (уровень 3) C4996](../../error-messages/compiler-warnings/compiler-warning-level-3-c4996.md). Имена являются устаревшими, так как они не соответствуют стандартным правилам C для имен, зависящих от реализации. Однако функции по-прежнему поддерживаются.

Вместо этого рекомендуется использовать [_strupr и _wcsupr](strupr-strupr-l-mbsupr-mbsupr-l-wcsupr-l-wcsupr.md) или улучшенные функции безопасности [_strupr_s и _wcsupr_s](strupr-s-strupr-s-l-mbsupr-s-mbsupr-s-l-wcsupr-s-wcsupr-s-l.md) . Вы также можете продолжать использовать эти имена функций и отключить предупреждение. Дополнительные сведения см. [в разделе Отключение](../../error-messages/compiler-warnings/compiler-warning-level-3-c4996.md#turn-off-the-warning) [имен функций](../../error-messages/compiler-warnings/compiler-warning-level-3-c4996.md#posix-function-names)Warning и POSIX.
