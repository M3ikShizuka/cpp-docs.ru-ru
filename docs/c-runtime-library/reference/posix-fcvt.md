---
description: 'Дополнительные сведения о: фквт'
title: fcvt
ms.date: 12/16/2019
api_name:
- fcvt
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
- fcvt
helpviewer_keywords:
- fcvt function
ms.assetid: 1f748ad0-e186-400e-af8e-80d4431523d7
ms.openlocfilehash: 2500d858e6fce640f6a8d8f009fb5d32895f7d29
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97117462"
---
# <a name="fcvt"></a>fcvt

Имя функции, определяемой корпорацией Майкрософт, `fcvt` является устаревшим псевдонимом для функции [_fcvt](fcvt.md) . По умолчанию он создает [Предупреждение компилятора (уровень 3) C4996](../../error-messages/compiler-warnings/compiler-warning-level-3-c4996.md). Имя является устаревшим, так как оно не соответствует стандартным правилам C для имен, зависящих от реализации. Однако функция по-прежнему поддерживается.

Вместо этого рекомендуется использовать [_fcvt](fcvt.md) или функцию [_fcvt_s](fcvt-s.md) с повышенным уровнем безопасности. Вы также можете продолжить использовать это имя функции и отключить предупреждение. Дополнительные сведения см. [в разделе Отключение](../../error-messages/compiler-warnings/compiler-warning-level-3-c4996.md#turn-off-the-warning) [имен функций](../../error-messages/compiler-warnings/compiler-warning-level-3-c4996.md#posix-function-names)Warning и POSIX.
