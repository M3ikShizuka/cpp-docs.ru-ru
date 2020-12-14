---
description: 'Дополнительные сведения о: фклосеалл'
title: fcloseall
ms.date: 12/16/2019
api_name:
- fcloseall
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
- fcloseall
helpviewer_keywords:
- fcloseall function
ms.assetid: 4f14acde-5bc5-43da-a709-7a3c559df3cf
ms.openlocfilehash: b54bf604adf4bd4d9c30a9c4d3a4c4e37ecbc99f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97235870"
---
# <a name="fcloseall"></a>fcloseall

Имя функции, определяемой корпорацией Майкрософт, `fcloseall` является устаревшим псевдонимом для функции [_fcloseall](fclose-fcloseall.md) . По умолчанию он создает [Предупреждение компилятора (уровень 3) C4996](../../error-messages/compiler-warnings/compiler-warning-level-3-c4996.md). Имя является устаревшим, так как оно не соответствует стандартным правилам C для имен, зависящих от реализации. Однако функция по-прежнему поддерживается.

Вместо этого рекомендуется использовать [_fcloseall](fclose-fcloseall.md) . Вы также можете продолжить использовать это имя функции и отключить предупреждение. Дополнительные сведения см. [в разделе Отключение](../../error-messages/compiler-warnings/compiler-warning-level-3-c4996.md#turn-off-the-warning) [имен функций](../../error-messages/compiler-warnings/compiler-warning-level-3-c4996.md#posix-function-names)Warning и POSIX.
