---
description: 'Дополнительные сведения о: лсик'
title: lseek
ms.date: 12/16/2019
api_name:
- lseek
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
- lseek
helpviewer_keywords:
- lseek function
ms.assetid: 137d7741-5c2e-443e-811a-6a01417fcae7
ms.openlocfilehash: 9f81e26d55e3ccedfc65d88f3d9f7605fe8cc894
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97299934"
---
# <a name="lseek"></a>lseek

Имя функции, реализованной корпорацией Майкрософт, `lseek` является устаревшим псевдонимом для функции [_lseek](lseek-lseeki64.md) . По умолчанию он создает [Предупреждение компилятора (уровень 3) C4996](../../error-messages/compiler-warnings/compiler-warning-level-3-c4996.md). Имя является устаревшим, так как оно не соответствует стандартным правилам C для имен, зависящих от реализации. Однако функция по-прежнему поддерживается.

Вместо этого рекомендуется использовать [_lseek](lseek-lseeki64.md) . Вы также можете продолжить использовать это имя функции и отключить предупреждение. Дополнительные сведения см. [в разделе Отключение](../../error-messages/compiler-warnings/compiler-warning-level-3-c4996.md#turn-off-the-warning) [имен функций](../../error-messages/compiler-warnings/compiler-warning-level-3-c4996.md#posix-function-names)Warning и POSIX.
