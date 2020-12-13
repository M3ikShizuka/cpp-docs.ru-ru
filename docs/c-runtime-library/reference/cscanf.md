---
description: 'Дополнительные сведения о: ксканф'
title: cscanf
ms.date: 12/16/2019
api_name:
- cscanf
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
- cscanf
helpviewer_keywords:
- cscanf function
ms.assetid: 51aa2da2-0d53-4272-b510-f3eabf049ea7
ms.openlocfilehash: 9f950dc89e29bcb87bdbfc6dcb3b72aa07f69017
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97332912"
---
# <a name="cscanf"></a>cscanf

Имя функции, определяемой корпорацией Майкрософт, `cscanf` является устаревшим псевдонимом для функции [_cscanf](cscanf-cscanf-l-cwscanf-cwscanf-l.md) . По умолчанию он создает [Предупреждение компилятора (уровень 3) C4996](../../error-messages/compiler-warnings/compiler-warning-level-3-c4996.md). Имя является устаревшим, так как оно не соответствует стандартным правилам C для имен, зависящих от реализации. Однако функция по-прежнему поддерживается.

Вместо этого рекомендуется использовать [_cscanf](cscanf-cscanf-l-cwscanf-cwscanf-l.md) . Вы также можете продолжить использовать это имя функции и отключить предупреждение. Дополнительные сведения см. [в разделе Отключение](../../error-messages/compiler-warnings/compiler-warning-level-3-c4996.md#turn-off-the-warning) [имен функций](../../error-messages/compiler-warnings/compiler-warning-level-3-c4996.md#posix-function-names)Warning и POSIX.

> [!IMPORTANT]
> Этот API нельзя использовать в приложениях, выполняемых в среде выполнения Windows. Дополнительные сведения: [Функции CRT, которые не поддерживаются в приложениях универсальной платформы Windows](../../cppcx/crt-functions-not-supported-in-universal-windows-platform-apps.md).
