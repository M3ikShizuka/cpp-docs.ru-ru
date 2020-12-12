---
description: 'Дополнительные сведения о: чсизе'
title: chsize
ms.date: 12/16/2019
api_name:
- chsize
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
- chsize
helpviewer_keywords:
- chsize function
ms.assetid: f94d62f6-b539-4cbf-bf99-b81d081b4216
ms.openlocfilehash: 1634239bbc2e98f9ce71fea4b59f646ebfbaee71
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97304653"
---
# <a name="chsize"></a>chsize

Имя функции, определяемой корпорацией Майкрософт, `chsize` является устаревшим псевдонимом для функции [_chsize](chsize.md) . По умолчанию он создает [Предупреждение компилятора (уровень 3) C4996](../../error-messages/compiler-warnings/compiler-warning-level-3-c4996.md). Имя является устаревшим, так как оно не соответствует стандартным правилам C для имен, зависящих от реализации. Однако функция по-прежнему поддерживается.

Вместо этого рекомендуется использовать [_chsize](chsize.md) или функцию [_chsize_s](chsize-s.md) с повышенным уровнем безопасности. Вы также можете продолжить использовать это имя функции и отключить предупреждение. Дополнительные сведения см. [в разделе Отключение](../../error-messages/compiler-warnings/compiler-warning-level-3-c4996.md#turn-off-the-warning) [имен функций](../../error-messages/compiler-warnings/compiler-warning-level-3-c4996.md#posix-function-names)Warning и POSIX.
