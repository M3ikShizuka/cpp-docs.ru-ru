---
description: 'Дополнительные сведения о: стррев, вксрев'
title: strrev, wcsrev
ms.date: 12/16/2019
api_name:
- strrev
- wcsrev
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
- strrev
- wcsrev
helpviewer_keywords:
- strrev function
- wcsrev function
ms.assetid: 89e05854-a9ce-4fb7-993d-a9831cd7edf2
ms.openlocfilehash: 2f9cb8e5a1a0bce09b0da030392d6b459f16c967
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97209429"
---
# <a name="strrev-wcsrev"></a>strrev, wcsrev

Имена функций, специфичных для Microsoft, `strrev` и `wcsrev` являются устаревшими псевдонимами для функций [_strrev и _wcsrev](strrev-wcsrev-mbsrev-mbsrev-l.md) . По умолчанию они генерируют [Предупреждение компилятора (уровень 3) C4996](../../error-messages/compiler-warnings/compiler-warning-level-3-c4996.md). Имена являются устаревшими, так как они не соответствуют стандартным правилам C для имен, зависящих от реализации. Однако функции по-прежнему поддерживаются.

Вместо этого рекомендуется использовать [_strrev и _wcsrev](strrev-wcsrev-mbsrev-mbsrev-l.md) . Вы также можете продолжать использовать эти имена функций и отключить предупреждение. Дополнительные сведения см. [в разделе Отключение](../../error-messages/compiler-warnings/compiler-warning-level-3-c4996.md#turn-off-the-warning) [имен функций](../../error-messages/compiler-warnings/compiler-warning-level-3-c4996.md#posix-function-names)Warning и POSIX.
