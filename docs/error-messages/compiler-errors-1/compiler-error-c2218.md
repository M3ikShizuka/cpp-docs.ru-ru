---
description: 'Дополнительные сведения о: Ошибка компилятора C2218'
title: Ошибка компилятора C2218
ms.date: 11/04/2016
f1_keywords:
- C2218
helpviewer_keywords:
- C2218
ms.assetid: b0f55da4-8edb-4b45-b298-1a091981bd7b
ms.openlocfilehash: d2761bb822c5a1055974e4a0bcd6011e7f451821
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97245529"
---
# <a name="compiler-error-c2218"></a>Ошибка компилятора C2218

> __vectorcall не может использоваться с /arch:IA32

**`__vectorcall`** Соглашение о вызовах поддерживается только в машинном коде на процессорах x86 и x64, включающих Streaming SIMD Extensions 2 (SSE2) и более поздних версий. Дополнительные сведения см. на веб-сайте [`__vectorcall`](../../cpp/vectorcall.md).

Чтобы устранить эту ошибку, измените параметры компилятора на целевые наборы инструкций SSE2, AVX или AVX2. Дополнительные сведения:  [`/arch` (x86)](../../build/reference/arch-x86.md).
