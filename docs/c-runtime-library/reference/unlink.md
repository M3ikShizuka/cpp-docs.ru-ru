---
description: 'Дополнительные сведения о: отмена связи'
title: unlink
ms.date: 12/16/2019
api_name:
- unlink
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
- unlink
helpviewer_keywords:
- unlink function
ms.assetid: 2cd82055-5770-48be-88ee-4b2c70541c46
ms.openlocfilehash: 2ea1c3b05d5e86807d774e07fb1c8ae7e56c6941
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97299375"
---
# <a name="unlink"></a>unlink

Имя функции, реализованной корпорацией Майкрософт, `unlink` является устаревшим псевдонимом для функции [_unlink](unlink-wunlink.md) . По умолчанию он создает [Предупреждение компилятора (уровень 3) C4996](../../error-messages/compiler-warnings/compiler-warning-level-3-c4996.md). Имя является устаревшим, так как оно не соответствует стандартным правилам C для имен, зависящих от реализации. Однако функция по-прежнему поддерживается.

Вместо этого рекомендуется использовать [_unlink](unlink-wunlink.md) . Вы также можете продолжить использовать это имя функции и отключить предупреждение. Дополнительные сведения см. [в разделе Отключение](../../error-messages/compiler-warnings/compiler-warning-level-3-c4996.md#turn-off-the-warning) [имен функций](../../error-messages/compiler-warnings/compiler-warning-level-3-c4996.md#posix-function-names)Warning и POSIX.
